---
title: "table.cell_set_text_font_family"
kind: function
namespace: table
source: https://www.tradingview.com/pine-script-reference/v6/#fun_table.cell_set_text_font_family
---

# table.cell_set_text_font_family

**Category:** Function

## Syntax

```pinescript
table.cell_set_text_font_family(table_id, column, row, text_font_family) → void
```

## Description

The function sets the font family of the text inside the cell.

## Arguments

- **`table_id`** `series table` — A table object.
- **`column`** `series int` — The index of the cell's column. Numbering starts at 0.
- **`row`** `series int` — The index of the cell's row. Numbering starts at 0.
- **`text_font_family`** `series string` — The font family of the text. Possible values: [font.family_default](../../constants/font/family_default.md), [font.family_monospace](../../constants/font/family_monospace.md).

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
indicator("Example of setting the table cell font")
var t = table.new(position.top_left, rows = 1, columns = 1)
table.cell(t, 0, 0, "monospace", text_color = color.blue)
table.cell_set_text_font_family(t, 0, 0, font.family_monospace)
```

## See also

- [table.new()](./new.md)
- [font.family_default](../../constants/font/family_default.md)
- [font.family_monospace](../../constants/font/family_monospace.md)
