---
title: "strategy.closedtrades.profit"
kind: function
namespace: strategy
source: https://www.tradingview.com/pine-script-reference/v6/#fun_strategy.closedtrades.profit
---

# strategy.closedtrades.profit

**Category:** Function

## Syntax

```pinescript
strategy.closedtrades.profit(trade_num) → series float
```

## Description

Returns the profit/loss of the closed trade in the strategy's account currency, reduced by the trade's commissions. A positive returned value represents a profit, and a negative value represents a loss.

## Arguments

- **`trade_num`** `series int` — The trade number of the closed trade. The number of the first trade is zero.

**Return type(s):** `series float`

## Examples

```pinescript
//@version=6
strategy("`strategy.closedtrades.profit()` example")

// Enter a long trade every 15 bars, and close a long trade every 20 bars.
if bar_index % 15 == 0
    strategy.entry("Long", strategy.long)
if bar_index % 20 == 0
    strategy.close("Long")

//@function Calculates the average gross profit from all available closed trades. 
avgGrossProfit() =>
    var float result = 0.0
    if result == 0.0 or strategy.closedtrades > strategy.closedtrades[1]
        float sumGrossProfit = 0.0
        for tradeNo = 0 to strategy.closedtrades - 1
            sumGrossProfit += strategy.closedtrades.profit(tradeNo)
        result := nz(sumGrossProfit / strategy.closedtrades)
    result

plot(avgGrossProfit(), "Average gross profit")
```

## See also

- [strategy.account_currency](../../variables/strategy/account_currency.md)
- [strategy.opentrades.profit()](./opentrades.profit.md)
- [strategy.closedtrades.commission()](./closedtrades.commission.md)
