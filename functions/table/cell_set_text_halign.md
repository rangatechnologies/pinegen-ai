---
title: "table.cell_set_text_halign"
kind: function
namespace: table
source: https://www.tradingview.com/pine-script-reference/v6/#fun_table.cell_set_text_halign
---

# table.cell_set_text_halign

**Category:** Function

## Syntax

```pinescript
table.cell_set_text_halign(table_id, column, row, text_halign) → void
```

## Description

The function sets the horizontal alignment of the cell's text.

## Arguments

- **`table_id`** `series table` — A table object.
- **`column`** `series int` — The index of the cell's column. Numbering starts at 0.
- **`row`** `series int` — The index of the cell's row. Numbering starts at 0.
- **`text_halign`** `series string` (optional) — The horizontal alignment of a cell's text. Possible values: [text.align_left](../../constants/text/align_left.md), [text.align_center](../../constants/text/align_center.md), [text.align_right](../../constants/text/align_right.md).

**Return type(s):** `void`

## See also

- [table.cell_set_bgcolor()](./cell_set_bgcolor.md)
- [table.cell_set_height()](./cell_set_height.md)
- [table.cell_set_text()](./cell_set_text.md)
- [table.cell_set_text_color()](./cell_set_text_color.md)
- [table.cell_set_text_size()](./cell_set_text_size.md)
- [table.cell_set_text_valign()](./cell_set_text_valign.md)
- [table.cell_set_width()](./cell_set_width.md)
- [table.cell_set_tooltip()](./cell_set_tooltip.md)
