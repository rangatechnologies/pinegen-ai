---
title: "strategy.convert_to_symbol"
kind: function
namespace: strategy
source: https://www.tradingview.com/pine-script-reference/v6/#fun_strategy.convert_to_symbol
---

# strategy.convert_to_symbol

**Category:** Function

## Syntax

```pinescript
strategy.convert_to_symbol(value) → series float
```

## Description

Converts the value from the currency used by the strategy ([strategy.account_currency](../../variables/strategy/account_currency.md)) to the currency that the symbol on the chart is traded in ([syminfo.currency](../../variables/syminfo/currency.md)).

## Arguments

- **`value`** `series int/float` — The value to be converted.

**Return type(s):** `series float`

## Examples

```pinescript
//@version=6
strategy("`strategy.convert_to_symbol` Example", currency = currency.EUR)

// Calculate the max qty we can buy using current chart's currency.
calcContracts(accountMoney) =>
    math.floor(strategy.convert_to_symbol(accountMoney) / syminfo.pointvalue / close)

// Return max qty we can buy using 300 euros
qt = calcContracts(300)

// Strategy calls to enter long trades every 15 bars and exit long trades every 20 bars using our custom qty.
if bar_index % 15 == 0
    strategy.entry("Long", strategy.long, qty = qt)
if bar_index % 20 == 0
    strategy.close("Long")
```

## See also

- [strategy()](../strategy.md)
- [strategy.convert_to_account()](./convert_to_account.md)
