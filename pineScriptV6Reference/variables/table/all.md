---
title: "table.all"
kind: variable
namespace: table
source: https://www.tradingview.com/pine-script-reference/v6/#var_table.all
---

# table.all

**Category:** Variable

**Type:** `array<table>`

## Description

Returns an array filled with all the current tables drawn by the script.

## Remarks

The array is read-only. Index zero of the array is the ID of the oldest object on the chart.

## Examples

```pinescript
//@version=6
indicator("table.all")
//delete all tables
table.new(position = position.top_right, columns = 2, rows = 1, bgcolor = color.yellow, border_width = 1)
a_allTables = table.all
if array.size(a_allTables) > 0
	for i = 0 to array.size(a_allTables) - 1
		table.delete(array.get(a_allTables, i))
```

## See also

- [table.new()](../../functions/table/new.md)
- [line.all](../line/all.md)
- [label.all](../label/all.md)
- [box.all](../box/all.md)
