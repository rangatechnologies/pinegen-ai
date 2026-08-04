---
title: "table"
kind: type
source: https://www.tradingview.com/pine-script-reference/v6/#type_table
---

# table

**Category:** Type

## Description

Keyword used to explicitly declare the "table" type of a variable or a parameter. Table objects (or IDs) can be created with the [table.new()](../functions/table/new.md) function.

## Remarks

Table objects are always of "series" form.

## Examples

```pinescript
//@version=6
indicator("table")
// Empty `table1` table ID.
var table table1 = na
// `table` type is unnecessary because `table.new()` returns "table" type.
var table2 = table.new(position.top_left, na, na)

if barstate.islastconfirmedhistory
	var table3 = table.new(position = position.top_right, columns = 1, rows = 1, bgcolor = color.yellow, border_width = 1)
	table.cell(table_id = table3, column = 0, row = 0, text = "table3 text")
```

## See also

- [var](../keywords/var.md)
- [line](./line.md)
- [label](./label.md)
- [box](./box.md)
- [table.new()](../functions/table/new.md)
