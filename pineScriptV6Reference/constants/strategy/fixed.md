---
title: "strategy.fixed"
kind: constant
namespace: strategy
source: https://www.tradingview.com/pine-script-reference/v6/#const_strategy.fixed
---

# strategy.fixed

**Category:** Constant

**Type:** `const string`

## Description

This is one of the arguments that can be supplied to the `default_qty_type` parameter in the [strategy()](../../functions/strategy.md) declaration statement. It is only relevant when no value is used for the ‘qty’ parameter in [strategy.entry()](../../functions/strategy/entry.md) or [strategy.order()](../../functions/strategy/order.md) function calls. It specifies that a number of contracts/shares/lots will be used to enter trades.

## Examples

```pinescript
//@version=6
strategy("strategy.fixed", overlay = true, default_qty_value = 50, default_qty_type = strategy.fixed, initial_capital = 1000000)

if bar_index == 0
    // As ‘qty’ is not defined, the previously defined values for the `default_qty_type` and `default_qty_value` parameters are used to enter trades, namely 50 contracts.
    // qty = 50
    strategy.entry("EN", strategy.long)
if bar_index == 2
    strategy.close("EN")
```

## See also

- [strategy()](../../functions/strategy.md)
