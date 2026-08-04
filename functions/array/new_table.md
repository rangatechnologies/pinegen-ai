---
title: "array.new_table"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.new_table
---

# array.new_table

**Category:** Function

## Syntax

```pinescript
array.new_table(size, initial_value) → array<table>
```

## Description

The function creates a new array object of table type elements.

## Arguments

- **`size`** `series int` (optional) — Initial size of an array. Optional. The default is 0.
- **`initial_value`** `series table` (optional) — Initial value of all array elements. Optional. The default is 'na'.

## Returns

The ID of an array object which may be used in other array.*() functions.

**Return type(s):** `array<table>`

## Remarks

An array index starts from 0.

## Examples

```pinescript
//@version=6
indicator("table array")
tables = array.new_table()
array.push(tables, table.new(position = position.top_left, rows = 1, columns = 2, bgcolor = color.yellow, border_width=1))
plot(1)
```

## See also

- [array.new_float()](./new_float.md)
- [array.get()](./get.md)
- [array.slice()](./slice.md)
