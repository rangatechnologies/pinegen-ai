---
title: "last_bar_index"
kind: variable
source: https://www.tradingview.com/pine-script-reference/v6/#var_last_bar_index
---

# last_bar_index

**Category:** Variable

**Type:** `series int`

## Description

Bar index of the last chart bar. Bar indices begin at zero on the first bar.

## Returns

Last historical bar index for closed markets, or the real-time bar index for open markets.

## Remarks

Please note that using this variable can cause [indicator repainting](https://www.tradingview.com/pine-script-docs/concepts/repainting/).

## Examples

```pinescript
//@version=6
strategy("Mark Last X Bars For Backtesting", overlay = true, calc_on_every_tick = true)
lastBarsFilterInput = input.int(100, "Bars Count:")
// Here, we store the 'last_bar_index' value that is known from the beginning of the script's calculation.
// The 'last_bar_index' will change when new real-time bars appear, so we declare 'lastbar' with the 'var' keyword.
var lastbar = last_bar_index
// Check if the current bar_index is 'lastBarsFilterInput' removed from the last bar on the chart, or the chart is traded in real-time.
allowedToTrade = (lastbar - bar_index <= lastBarsFilterInput) or barstate.isrealtime
bgcolor(allowedToTrade ? color.new(color.green, 80) : na)
```

## See also

- [bar_index](./bar_index.md)
- [last_bar_time](./last_bar_time.md)
- [barstate.ishistory](./barstate/ishistory.md)
- [barstate.isrealtime](./barstate/isrealtime.md)
