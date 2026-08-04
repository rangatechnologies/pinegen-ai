---
title: "strategy.closedtrades.max_drawdown"
kind: function
namespace: strategy
source: https://www.tradingview.com/pine-script-reference/v6/#fun_strategy.closedtrades.max_drawdown
---

# strategy.closedtrades.max_drawdown

**Category:** Function

## Syntax

```pinescript
strategy.closedtrades.max_drawdown(trade_num) → series float
```

## Description

Returns the maximum drawdown of the closed trade, i.e., the maximum possible loss during the trade, expressed in [strategy.account_currency](../../variables/strategy/account_currency.md).

## Arguments

- **`trade_num`** `series int` — The trade number of the closed trade. The number of the first trade is zero.

**Return type(s):** `series float`

## Remarks

The function returns na if trade_num is not in the range: 0 to strategy.closedtrades - 1.

## Examples

```pinescript
//@version=6
strategy("`strategy.closedtrades.max_drawdown` Example")

// Strategy calls to enter long trades every 15 bars and exit long trades every 20 bars.
if bar_index % 15 == 0
    strategy.entry("Long", strategy.long)
if bar_index % 20 == 0
    strategy.close("Long")

// Get the biggest max trade drawdown value from all of the closed trades.
maxTradeDrawDown() =>
    maxDrawdown = 0.0
    for tradeNo = 0 to strategy.closedtrades - 1
        maxDrawdown := math.max(maxDrawdown, strategy.closedtrades.max_drawdown(tradeNo))
    result = maxDrawdown

plot(maxTradeDrawDown(), "Biggest max drawdown")
```

## See also

- [strategy.opentrades.max_drawdown()](./opentrades.max_drawdown.md)
- [strategy.max_drawdown](../../variables/strategy/max_drawdown.md)
