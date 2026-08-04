---
title: "table.cell_set_text_size"
kind: function
namespace: table
source: https://www.tradingview.com/pine-script-reference/v6/#fun_table.cell_set_text_size
---

# table.cell_set_text_size

**Category:** Function

## Syntax

```pinescript
table.cell_set_text_size(table_id, column, row, text_size) → void
```

## Description

The function sets the size of the cell's text.

## Arguments

- **`table_id`** `series table` — A table object.
- **`column`** `series int` — The index of the cell's column. Numbering starts at 0.
- **`row`** `series int` — The index of the cell's row. Numbering starts at 0.
- **`text_size`** `series int/string` (optional) — Size of the object. The size can be any positive integer, or one of the size.* built-in constant strings. The constant strings and their equivalent integer values are: [size.auto](../../constants/size/auto.md) (0), [size.tiny](../../constants/size/tiny.md) (8), [size.small](../../constants/size/small.md) (10), [size.normal](../../constants/size/normal.md) (14), [size.large](../../constants/size/large.md) (20), [size.huge](../../constants/size/huge.md) (36). The default value is [size.normal](../../constants/size/normal.md) or 14.

**Return type(s):** `void`

## See also

- [table.cell_set_bgcolor()](./cell_set_bgcolor.md)
- [table.cell_set_height()](./cell_set_height.md)
- [table.cell_set_text()](./cell_set_text.md)
- [table.cell_set_text_color()](./cell_set_text_color.md)
- [table.cell_set_text_halign()](./cell_set_text_halign.md)
- [table.cell_set_text_valign()](./cell_set_text_valign.md)
- [table.cell_set_width()](./cell_set_width.md)
- [table.cell_set_tooltip()](./cell_set_tooltip.md)
