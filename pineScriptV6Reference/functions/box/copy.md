---
title: "box.copy"
kind: function
namespace: box
source: https://www.tradingview.com/pine-script-reference/v6/#fun_box.copy
---

# box.copy

**Category:** Function

## Syntax

```pinescript
box.copy(id) → series box
```

## Description

Clones the box object.

## Arguments

- **`id`** `series box` — Box object.

**Return type(s):** `series box`

## Examples

```pinescript
//@version=6
indicator('Last 50 bars price ranges', overlay = true)
LOOKBACK = 50
highest = ta.highest(LOOKBACK)
lowest = ta.lowest(LOOKBACK)
if barstate.islastconfirmedhistory
	var BoxLast = box.new(bar_index[LOOKBACK], highest, bar_index, lowest, bgcolor = color.new(color.green, 80))
	var BoxPrev = box.copy(BoxLast)
	box.set_lefttop(BoxPrev, bar_index[LOOKBACK * 2], highest[50])
	box.set_rightbottom(BoxPrev, bar_index[LOOKBACK], lowest[50])
	box.set_bgcolor(BoxPrev, color.new(color.red, 80))
```

## See also

- [box.new()](./new.md)
- [box.delete()](./delete.md)
