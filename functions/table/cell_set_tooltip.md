---
title: "table.cell_set_tooltip"
kind: function
namespace: table
source: https://www.tradingview.com/pine-script-reference/v6/#fun_table.cell_set_tooltip
---

# table.cell_set_tooltip

**Category:** Function

## Syntax

```pinescript
table.cell_set_tooltip(table_id, column, row, tooltip) → void
```

## Description

The function sets the tooltip in the specified cell.

## Arguments

- **`table_id`** `series table` — A table object.
- **`column`** `series int` — The index of the cell's column. Numbering starts at 0.
- **`row`** `series int` — The index of the cell's row. Numbering starts at 0.
- **`tooltip`** `series string` (optional) — The tooltip to be displayed inside the cell.

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
indicator("TABLE example")
var tLog = table.new(position = position.top_left, rows = 1, columns = 2, bgcolor = color.yellow, border_width=1)
table.cell(tLog, row = 0, column = 0, text = "sometext", text_color = color.blue)
table.cell_set_tooltip(tLog, row = 0, column = 0, tooltip = "sometext")
```

## See also

- [table.cell_set_bgcolor()](./cell_set_bgcolor.md)
- [table.cell_set_height()](./cell_set_height.md)
- [table.cell_set_text_color()](./cell_set_text_color.md)
- [table.cell_set_text_halign()](./cell_set_text_halign.md)
- [table.cell_set_text_size()](./cell_set_text_size.md)
- [table.cell_set_text_valign()](./cell_set_text_valign.md)
- [table.cell_set_width()](./cell_set_width.md)
- [table.cell_set_text()](./cell_set_text.md)
