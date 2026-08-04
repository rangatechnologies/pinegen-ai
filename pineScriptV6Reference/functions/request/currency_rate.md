---
title: "request.currency_rate"
kind: function
namespace: request
source: https://www.tradingview.com/pine-script-reference/v6/#fun_request.currency_rate
---

# request.currency_rate

**Category:** Function

## Syntax

```pinescript
request.currency_rate(from, to, ignore_invalid_currency) → series float
```

## Description

Provides a daily rate that can be used to convert a value expressed in the `from` currency to another in the `to` currency.

## Arguments

- **`from`** `series string` — The currency in which the value to be converted is expressed. Possible values: a three-letter string with the [currency code in the ISO 4217 format](https://en.wikipedia.org/wiki/ISO_4217#Active_codes) (e.g. "USD"), or one of the built-in variables that return currency codes, like [syminfo.currency](../../variables/syminfo/currency.md) or [currency.USD](../../constants/currency/usd.md).
- **`to`** `series string` — The currency in which the value is to be converted. Possible values: a three-letter string with the [currency code in the ISO 4217 format](https://en.wikipedia.org/wiki/ISO_4217#Active_codes) (e.g. "USD"), or one of the built-in variables that return currency codes, like [syminfo.currency](../../variables/syminfo/currency.md) or [currency.USD](../../constants/currency/usd.md).
- **`ignore_invalid_currency`** `series bool` (optional) — Determines the behavior of the function if a conversion rate between the two currencies cannot be calculated: if [false](../../constants/false.md), the script will halt and return a runtime error; if [true](../../constants/true.md), the function will return [na](../../variables/na.md) and execution will continue. Optional. The default is [false](../../constants/false.md).

**Return type(s):** `series float`

## Remarks

If `from` and `to` arguments are equal, function returns 1. Please note that using this variable/function can cause [indicator repainting](https://www.tradingview.com/pine-script-docs/concepts/repainting/).

## Examples

```pinescript
//@version=6
indicator("Close in British Pounds")
rate = request.currency_rate(syminfo.currency, "GBP")
plot(close * rate)
```
