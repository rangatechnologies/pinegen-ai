---
title: "strategy.closedtrades.entry_time"
kind: function
namespace: strategy
source: https://www.tradingview.com/pine-script-reference/v6/#fun_strategy.closedtrades.entry_time
---

# strategy.closedtrades.entry_time

**Category:** Function

## Syntax

```pinescript
strategy.closedtrades.entry_time(trade_num) → series int
```

## Description

Returns the UNIX time of the closed trade's entry, expressed in milliseconds..

## Arguments

- **`trade_num`** `series int` — The trade number of the closed trade. The number of the first trade is zero.

**Return type(s):** `series int`

## Examples

```pinescript
//@version=6
strategy("strategy.closedtrades.entry_time Example", overlay = true)

// Enter long trades on three rising bars; exit on two falling bars.
if ta.rising(close, 3)
    strategy.entry("Long", strategy.long)
if ta.falling(close, 2)
    strategy.close("Long")

// Calculate the average trade duration
avgTradeDuration() =>
    sumTradeDuration = 0
    for i = 0 to strategy.closedtrades - 1
        sumTradeDuration += strategy.closedtrades.exit_time(i) - strategy.closedtrades.entry_time(i)
    result = nz(sumTradeDuration / strategy.closedtrades)

// Display average duration converted to seconds and formatted using 2 decimal points
if barstate.islastconfirmedhistory
    label.new(bar_index, high, str.tostring(avgTradeDuration() / 1000, "#.##") + " seconds")
```

## See also

- [strategy.opentrades.entry_time()](./opentrades.entry_time.md)
- [strategy.closedtrades.exit_time()](./closedtrades.exit_time.md)
- [time](../../variables/time.md)
