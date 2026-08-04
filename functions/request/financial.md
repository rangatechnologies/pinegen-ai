---
title: "request.financial"
kind: function
namespace: request
source: https://www.tradingview.com/pine-script-reference/v6/#fun_request.financial
---

# request.financial

**Category:** Function

## Syntax

```pinescript
request.financial(symbol, financial_id, period, gaps, ignore_invalid_symbol, currency) → series float
```

## Description

Requests financial series for symbol.

## Arguments

- **`symbol`** `series string` — Symbol. Note that the symbol should be passed with a prefix. For example: "NASDAQ:AAPL" instead of "AAPL".
- **`financial_id`** `series string` — Financial identifier. You can find the list of available ids via our [Help Center](https://www.tradingview.com/?solution=43000564727).
- **`period`** `series string` — Reporting period. Possible values are "TTM", "FY", "FQ", "FH", "D".
- **`gaps`** `simple barmerge_gaps` (optional) — Merge strategy for the requested data (requested data automatically merges with the main series: OHLC data). Possible values include: [barmerge.gaps_on](../../constants/barmerge/gaps_on.md), [barmerge.gaps_off](../../constants/barmerge/gaps_off.md). [barmerge.gaps_on](../../constants/barmerge/gaps_on.md) - requested data is merged with possible gaps ([na](../../variables/na.md) values). [barmerge.gaps_off](../../constants/barmerge/gaps_off.md) - requested data is merged continuously without gaps, all the gaps are filled with the previous, nearest existing values. Default value is [barmerge.gaps_off](../../constants/barmerge/gaps_off.md).
- **`ignore_invalid_symbol`** `input bool` (optional) — An optional parameter. Determines the behavior of the function if the specified symbol is not found: if false, the script will halt and return a runtime error; if true, the function will return na and execution will continue. The default value is false.
- **`currency`** `series string` (optional) — Optional. Currency into which the symbol's financial metrics (e.g. Net Income) are to be converted. The conversion rate depends on the previous daily value of a corresponding currency pair from the most popular exchange. A spread symbol is used if no exchange provides the rate directly. Possible values: a "string" representing a valid currency code (e.g., "USD" or "USDT") or a constant from the `currency.*` namespace (e.g., [currency.USD](../../constants/currency/usd.md) or [currency.USDT](../../constants/currency/usdt.md)). The default is [syminfo.currency](../../variables/syminfo/currency.md).

## Returns

Requested series.

**Return type(s):** `series float`

## Examples

```pinescript
//@version=6
indicator("request.financial")
f = request.financial("NASDAQ:MSFT", "ACCOUNTS_PAYABLE", "FY")
plot(f)
```

## See also

- [request.security()](./security.md)
- [syminfo.tickerid](../../variables/syminfo/tickerid.md)
