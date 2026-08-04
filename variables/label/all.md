---
title: "label.all"
kind: variable
namespace: label
source: https://www.tradingview.com/pine-script-reference/v6/#var_label.all
---

# label.all

**Category:** Variable

**Type:** `array<label>`

## Description

Returns an array filled with all the current labels drawn by the script.

## Remarks

The array is read-only. Index zero of the array is the ID of the oldest object on the chart.

## Examples

```pinescript
//@version=6
indicator("label.all")
//delete all labels
label.new(bar_index, close)
a_allLabels = label.all
if array.size(a_allLabels) > 0
	for i = 0 to array.size(a_allLabels) - 1
		label.delete(array.get(a_allLabels, i))
```

## See also

- [label.new()](../../functions/label/new.md)
- [line.all](../line/all.md)
- [box.all](../box/all.md)
- [table.all](../table/all.md)
