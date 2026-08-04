---
title: "table.new"
kind: function
namespace: table
source: https://www.tradingview.com/pine-script-reference/v6/#fun_table.new
---

# table.new

**Category:** Function

## Syntax

```pinescript
table.new(position, columns, rows, bgcolor, frame_color, frame_width, border_color, border_width, force_overlay) → series table
```

## Description

The function creates a new table.

## Arguments

- **`position`** `series string` — Position of the table. Possible values are: [position.top_left](../../constants/position/top_left.md), [position.top_center](../../constants/position/top_center.md), [position.top_right](../../constants/position/top_right.md), [position.middle_left](../../constants/position/middle_left.md), [position.middle_center](../../constants/position/middle_center.md), [position.middle_right](../../constants/position/middle_right.md), [position.bottom_left](../../constants/position/bottom_left.md), [position.bottom_center](../../constants/position/bottom_center.md), [position.bottom_right](../../constants/position/bottom_right.md).
- **`columns`** `series int` — The number of columns in the table.
- **`rows`** `series int` — The number of rows in the table.
- **`bgcolor`** `series color` (optional) — The background color of the table. Optional. The default is no color.
- **`frame_color`** `series color` (optional) — The color of the outer frame of the table. Optional. The default is no color.
- **`frame_width`** `series int` (optional) — The width of the outer frame of the table. Optional. The default is 0.
- **`border_color`** `series color` (optional) — The color of the borders of the cells (excluding the outer frame). Optional. The default is no color.
- **`border_width`** `series int` (optional) — The width of the borders of the cells (excluding the outer frame). Optional. The default is 0.
- **`force_overlay`** `const bool` (optional) — If [true](../../constants/true.md), the drawing will display on the main chart pane, even when the script occupies a separate pane. Optional. The default is [false](../../constants/false.md).

## Returns

The ID of a table object that can be passed to other table.*() functions.

**Return type(s):** `series table`

## Remarks

This function creates the table object itself, but the table will not be displayed until its cells are populated. To define a cell and change its contents or attributes, use [table.cell()](./cell.md) and other table.cell_*() functions.

One [table.new()](./new.md) call can only display one table (the last one drawn), but the function itself will be recalculated on each bar it is used on. For performance reasons, it is wise to use [table.new()](./new.md) in conjunction with either the [var](../../keywords/var.md) keyword (so the table object is only created on the first bar) or in an [if](../../keywords/if.md) [barstate.islast](../../variables/barstate/islast.md) block (so the table object is only created on the last bar).

## Examples

```pinescript
//@version=6
indicator("table.new example")
var testTable = table.new(position = position.top_right, columns = 2, rows = 1, bgcolor = color.yellow, border_width = 1)
if barstate.islast
    table.cell(table_id = testTable, column = 0, row = 0, text = "Open is " + str.tostring(open))
    table.cell(table_id = testTable, column = 1, row = 0, text = "Close is " + str.tostring(close), bgcolor=color.teal)
```

## See also

- [table.cell()](./cell.md)
- [table.clear()](./clear.md)
- [table.delete()](./delete.md)
- [table.set_bgcolor()](./set_bgcolor.md)
- [table.set_border_color()](./set_border_color.md)
- [table.set_border_width()](./set_border_width.md)
- [table.set_frame_color()](./set_frame_color.md)
- [table.set_frame_width()](./set_frame_width.md)
- [table.set_position()](./set_position.md)
