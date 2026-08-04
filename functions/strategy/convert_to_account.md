---
title: "strategy.convert_to_account"
kind: function
namespace: strategy
source: https://www.tradingview.com/pine-script-reference/v6/#fun_strategy.convert_to_account
---

# strategy.convert_to_account

**Category:** Function

## Syntax

```pinescript
strategy.convert_to_account(value) → series float
```

## Description

Converts the value from the currency that the symbol on the chart is traded in ([syminfo.currency](../../variables/syminfo/currency.md)) to the currency used by the strategy ([strategy.account_currency](../../variables/strategy/account_currency.md)).

## Arguments

- **`value`** `series int/float` — The value to be converted.

**Return type(s):** `series float`

## Detailed Description



```pinescript
//@version=6
strategy("`strategy.convert_to_account` Example 1", currency = currency.EUR)

plot(close, "Close price using default currency")
plot(strategy.convert_to_account(close), "Close price converted to strategy currency")
```

---



```pinescript
// Calculates the "Buy and hold return" using your account's currency.
//@version=6
strategy("`strategy.convert_to_account` Example 2", currency = currency.EUR)

dateInput = input.time(timestamp("20 Jul 2021 00:00 +0300"), "From Date", confirm = true)

buyAndHoldReturnPct(fromDate) =>
    if time >= fromDate
        money = close * syminfo.pointvalue
        var initialBal = strategy.convert_to_account(money)
        (strategy.convert_to_account(money) - initialBal) / initialBal * 100

plot(buyAndHoldReturnPct(dateInput))
```

## See also

- [strategy()](../strategy.md)
- [strategy.convert_to_symbol()](./convert_to_symbol.md)
