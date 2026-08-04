---
title: "strategy.closedtrades.entry_bar_index"
kind: function
namespace: strategy
source: https://www.tradingview.com/pine-script-reference/v6/#fun_strategy.closedtrades.entry_bar_index
---

# strategy.closedtrades.entry_bar_index

**Category:** Function

## Syntax

```pinescript
strategy.closedtrades.entry_bar_index(trade_num) → series int
```

## Description

Returns the bar_index of the closed trade's entry.

## Arguments

- **`trade_num`** `series int` — The trade number of the closed trade. The number of the first trade is zero.

**Return type(s):** `series int`

## Examples

```pinescript
//@version=6
strategy("strategy.closedtrades.entry_bar_index Example")
// Enter long trades on three rising bars; exit on two falling bars.
if ta.rising(close, 3)
    strategy.entry("Long", strategy.long)
if ta.falling(close, 2)
    strategy.close("Long")
// Function that calculates the average amount of bars in a trade.
avgBarsPerTrade() =>
	sumBarsPerTrade = 0
	for tradeNo = 0 to strategy.closedtrades - 1
		// Loop through all closed trades, starting with the oldest.
		sumBarsPerTrade += strategy.closedtrades.exit_bar_index(tradeNo) - strategy.closedtrades.entry_bar_index(tradeNo) + 1
	result = nz(sumBarsPerTrade / strategy.closedtrades)
plot(avgBarsPerTrade())
```

## See also

- [strategy.closedtrades.exit_bar_index()](./closedtrades.exit_bar_index.md)
- [strategy.opentrades.entry_bar_index()](./opentrades.entry_bar_index.md)
