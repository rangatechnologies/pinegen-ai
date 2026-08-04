---
title: "line.all"
kind: variable
namespace: line
source: https://www.tradingview.com/pine-script-reference/v6/#var_line.all
---

# line.all

**Category:** Variable

**Type:** `array<line>`

## Description

Returns an array filled with all the current lines drawn by the script.

## Remarks

The array is read-only. Index zero of the array is the ID of the oldest object on the chart.

## Examples

```pinescript
//@version=6
indicator("line.all")
//delete all lines
line.new(bar_index - 10, close, bar_index, close)
a_allLines = line.all
if array.size(a_allLines) > 0
	for i = 0 to array.size(a_allLines) - 1
		line.delete(array.get(a_allLines, i))
```

## See also

- [line.new()](../../functions/line/new.md)
- [label.all](../label/all.md)
- [box.all](../box/all.md)
- [table.all](../table/all.md)
