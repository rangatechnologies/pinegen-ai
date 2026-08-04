---
title: "table.cell_set_height"
kind: function
namespace: table
source: https://www.tradingview.com/pine-script-reference/v6/#fun_table.cell_set_height
---

# table.cell_set_height

**Category:** Function

## Syntax

```pinescript
table.cell_set_height(table_id, column, row, height) → void
```

## Description

The function sets the height of cell.

## Arguments

- **`table_id`** `series table` — A table object.
- **`column`** `series int` — The index of the cell's column. Numbering starts at 0.
- **`row`** `series int` — The index of the cell's row. Numbering starts at 0.
- **`height`** `series int/float` (optional) — The height of the cell as a % of the chart window. Passing 0 auto-adjusts the height based on the text inside of the cell.

**Return type(s):** `void`

## See also

- [table.cell_set_bgcolor()](./cell_set_bgcolor.md)
- [table.cell_set_text()](./cell_set_text.md)
- [table.cell_set_text_color()](./cell_set_text_color.md)
- [table.cell_set_text_halign()](./cell_set_text_halign.md)
- [table.cell_set_text_size()](./cell_set_text_size.md)
- [table.cell_set_text_valign()](./cell_set_text_valign.md)
- [table.cell_set_width()](./cell_set_width.md)
- [table.cell_set_tooltip()](./cell_set_tooltip.md)
