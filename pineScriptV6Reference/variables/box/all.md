---
title: "box.all"
kind: variable
namespace: box
source: https://www.tradingview.com/pine-script-reference/v6/#var_box.all
---

# box.all

**Category:** Variable

**Type:** `array<box>`

## Description

Returns an array filled with all the current boxes drawn by the script.

## Remarks

The array is read-only. Index zero of the array is the ID of the oldest object on the chart.

## Examples

```pinescript
//@version=6
indicator("box.all")
//delete all boxes
box.new(time, open, time + 60 * 60 * 24, close, xloc=xloc.bar_time, border_style=line.style_dashed)
a_allBoxes = box.all
if array.size(a_allBoxes) > 0
	for i = 0 to array.size(a_allBoxes) - 1
		box.delete(array.get(a_allBoxes, i))
```

## See also

- [box.new()](../../functions/box/new.md)
- [line.all](../line/all.md)
- [label.all](../label/all.md)
- [table.all](../table/all.md)
