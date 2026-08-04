---
title: "strategy.closedtrades.commission"
kind: function
namespace: strategy
source: https://www.tradingview.com/pine-script-reference/v6/#fun_strategy.closedtrades.commission
---

# strategy.closedtrades.commission

**Category:** Function

## Syntax

```pinescript
strategy.closedtrades.commission(trade_num) → series float
```

## Description

Returns the sum of entry and exit fees paid in the closed trade, expressed in [strategy.account_currency](../../variables/strategy/account_currency.md).

## Arguments

- **`trade_num`** `series int` — The trade number of the closed trade. The number of the first trade is zero.

**Return type(s):** `series float`

## Examples

```pinescript
//@version=6
strategy("`strategy.closedtrades.commission` Example", commission_type = strategy.commission.percent, commission_value = 0.1)

// Strategy calls to enter long trades every 15 bars and exit long trades every 20 bars.
if bar_index % 15 == 0
    strategy.entry("Long", strategy.long)
if bar_index % 20 == 0
    strategy.close("Long")

// Plot total fees for the latest closed trade.
plot(strategy.closedtrades.commission(strategy.closedtrades - 1))
```

## See also

- [strategy()](../strategy.md)
- [strategy.opentrades.commission()](./opentrades.commission.md)
