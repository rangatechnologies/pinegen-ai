---
title: "table.clear"
kind: function
namespace: table
source: https://www.tradingview.com/pine-script-reference/v6/#fun_table.clear
---

# table.clear

**Category:** Function

## Syntax

```pinescript
table.clear(table_id, start_column, start_row, end_column, end_row) → void
```

## Description

The function removes a cell or a sequence of cells from the table. The cells are removed in a rectangle shape where the start_column and start_row specify the top-left corner, and end_column and end_row specify the bottom-right corner.

## Arguments

- **`table_id`** `series table` — A table object.
- **`start_column`** `series int` — The index of the column of the first cell to delete. Numbering starts at 0.
- **`start_row`** `series int` — The index of the row of the first cell to delete. Numbering starts at 0.
- **`end_column`** `series int` (optional) — The index of the column of the last cell to delete. Optional. The default is the argument used for start_column. Numbering starts at 0.
- **`end_row`** `series int` (optional) — The index of the row of the last cell to delete. Optional. The default is the argument used for start_row. Numbering starts at 0.

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
indicator("A donut", overlay=true)
if barstate.islast
    colNum = 8, rowNum = 8
    padding = "◯"
    donutTable = table.new(position.middle_right, colNum, rowNum)
    for c = 0 to colNum - 1
        for r = 0 to rowNum - 1
            table.cell(donutTable, c, r, text=padding, bgcolor=#face6e, text_color=color.new(color.black, 100))
    table.clear(donutTable, 2, 2, 5, 5)
```

## See also

- [table.delete()](./delete.md)
- [table.new()](./new.md)
