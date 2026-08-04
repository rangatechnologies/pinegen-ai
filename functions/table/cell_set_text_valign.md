---
title: "table.cell_set_text_valign"
kind: function
namespace: table
source: https://www.tradingview.com/pine-script-reference/v6/#fun_table.cell_set_text_valign
---

# table.cell_set_text_valign

**Category:** Function

## Syntax

```pinescript
table.cell_set_text_valign(table_id, column, row, text_valign) → void
```

## Description

The function sets the vertical alignment of a cell's text.

## Arguments

- **`table_id`** `series table` — A table object.
- **`column`** `series int` — The index of the cell's column. Numbering starts at 0.
- **`row`** `series int` — The index of the cell's row. Numbering starts at 0.
- **`text_valign`** `series string` (optional) — The vertical alignment of the cell's text. Possible values: [text.align_top](../../constants/text/align_top.md), [text.align_center](../../constants/text/align_center.md), [text.align_bottom](../../constants/text/align_bottom.md).

**Return type(s):** `void`

## See also

- [table.cell_set_bgcolor()](./cell_set_bgcolor.md)
- [table.cell_set_height()](./cell_set_height.md)
- [table.cell_set_text()](./cell_set_text.md)
- [table.cell_set_text_color()](./cell_set_text_color.md)
- [table.cell_set_text_halign()](./cell_set_text_halign.md)
- [table.cell_set_text_size()](./cell_set_text_size.md)
- [table.cell_set_width()](./cell_set_width.md)
- [table.cell_set_tooltip()](./cell_set_tooltip.md)
