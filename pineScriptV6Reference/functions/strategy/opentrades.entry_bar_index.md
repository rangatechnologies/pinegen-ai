---
title: "strategy.opentrades.entry_bar_index"
kind: function
namespace: strategy
source: https://www.tradingview.com/pine-script-reference/v6/#fun_strategy.opentrades.entry_bar_index
---

# strategy.opentrades.entry_bar_index

**Category:** Function

## Syntax

```pinescript
strategy.opentrades.entry_bar_index(trade_num) → series int
```

## Description

Returns the bar_index of the open trade's entry.

## Arguments

- **`trade_num`** `series int` — The trade number of the open trade. The number of the first trade is zero.

**Return type(s):** `series int`

## Detailed Description



```pinescript
// Wait 10 bars and then close the position.
//@version=6
strategy("`strategy.opentrades.entry_bar_index` Example")

barsSinceLastEntry() =>
    strategy.opentrades > 0 ? bar_index - strategy.opentrades.entry_bar_index(strategy.opentrades - 1) : na

// Enter a long position if there are no open positions.
if strategy.opentrades == 0
    strategy.entry("Long", strategy.long)

// Close the long position after 10 bars.
if barsSinceLastEntry() >= 10
    strategy.close("Long")
```

## See also

- [strategy.closedtrades.entry_bar_index()](./closedtrades.entry_bar_index.md)
- [strategy.closedtrades.exit_bar_index()](./closedtrades.exit_bar_index.md)
