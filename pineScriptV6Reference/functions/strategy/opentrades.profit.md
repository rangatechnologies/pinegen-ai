---
title: "strategy.opentrades.profit"
kind: function
namespace: strategy
source: https://www.tradingview.com/pine-script-reference/v6/#fun_strategy.opentrades.profit
---

# strategy.opentrades.profit

**Category:** Function

## Syntax

```pinescript
strategy.opentrades.profit(trade_num) → series float
```

## Description

Returns the profit/loss of the open trade, expressed in [strategy.account_currency](../../variables/strategy/account_currency.md). Losses are expressed as negative values.

## Arguments

- **`trade_num`** `series int` — The trade number of the open trade. The number of the first trade is zero.

**Return type(s):** `series float`

## Detailed Description



```pinescript
// Returns the profit of the last open trade.
//@version=6
strategy("`strategy.opentrades.profit` Example 1", commission_type = strategy.commission.percent, commission_value = 0.1)

// Strategy calls to enter long trades every 15 bars and exit long trades every 20 bars.
if bar_index % 15 == 0
    strategy.entry("Long", strategy.long)
if bar_index % 20 == 0
    strategy.close("Long")

plot(strategy.opentrades.profit(strategy.opentrades - 1), "Profit of the latest open trade")
```

---



```pinescript
// Calculates the profit for all open trades.
//@version=6
strategy("`strategy.opentrades.profit` Example 2", pyramiding = 5)

// Strategy calls to enter 5 long positions every 2 bars.
if bar_index % 2 == 0
    strategy.entry("Long", strategy.long, qty = 5)

// Calculate open profit or loss for the open positions.
tradeOpenPL() =>
    sumProfit = 0.0
    for tradeNo = 0 to strategy.opentrades - 1
        sumProfit += strategy.opentrades.profit(tradeNo)
    result = sumProfit

plot(tradeOpenPL(), "Profit of all open trades")
```

## See also

- [strategy.closedtrades.profit()](./closedtrades.profit.md)
- [strategy.openprofit](../../variables/strategy/openprofit.md)
- [strategy.netprofit](../../variables/strategy/netprofit.md)
- [strategy.grossprofit](../../variables/strategy/grossprofit.md)
