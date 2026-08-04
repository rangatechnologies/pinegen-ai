---
title: "table.cell"
kind: function
namespace: table
source: https://www.tradingview.com/pine-script-reference/v6/#fun_table.cell
---

# table.cell

**Category:** Function

## Syntax

```pinescript
table.cell(table_id, column, row, text, width, height, text_color, text_halign, text_valign, text_size, bgcolor, tooltip, text_font_family, text_formatting) → void
```

## Description

The function defines a cell in the table and sets its attributes.

## Arguments

- **`table_id`** `series table` — A table object.
- **`column`** `series int` — The index of the cell's column. Numbering starts at 0.
- **`row`** `series int` — The index of the cell's row. Numbering starts at 0.
- **`text`** `series string` (optional) — The text to be displayed inside the cell. Optional. The default is empty string.
- **`width`** `series int/float` (optional) — The width of the cell as a % of the indicator's visual space. Optional. By default, auto-adjusts the width based on the text inside the cell. Value 0 has the same effect.
- **`height`** `series int/float` (optional) — The height of the cell as a % of the indicator's visual space. Optional. By default, auto-adjusts the height based on the text inside of the cell. Value 0 has the same effect.
- **`text_color`** `series color` (optional) — The color of the text. Optional. The default is [color.black](../../constants/color/black.md).
- **`text_halign`** `series string` (optional) — The horizontal alignment of the cell's text. Optional. The default value is [text.align_center](../../constants/text/align_center.md). Possible values: [text.align_left](../../constants/text/align_left.md), [text.align_center](../../constants/text/align_center.md), [text.align_right](../../constants/text/align_right.md).
- **`text_valign`** `series string` (optional) — The vertical alignment of the cell's text. Optional. The default value is [text.align_center](../../constants/text/align_center.md). Possible values: [text.align_top](../../constants/text/align_top.md), [text.align_center](../../constants/text/align_center.md), [text.align_bottom](../../constants/text/align_bottom.md).
- **`text_size`** `series int/string` (optional) — Size of the object. The size can be any positive integer, or one of the size.* built-in constant strings. The constant strings and their equivalent integer values are: [size.auto](../../constants/size/auto.md) (0), [size.tiny](../../constants/size/tiny.md) (8), [size.small](../../constants/size/small.md) (10), [size.normal](../../constants/size/normal.md) (14), [size.large](../../constants/size/large.md) (20), [size.huge](../../constants/size/huge.md) (36). The default value is [size.normal](../../constants/size/normal.md) or 14.
- **`bgcolor`** `series color` (optional) — The background color of the text. Optional. The default is no color.
- **`tooltip`** `series string` (optional) — The tooltip to be displayed inside the cell. Optional.
- **`text_font_family`** `series string` (optional) — The font family of the text. Optional. The default value is [font.family_default](../../constants/font/family_default.md). Possible values: [font.family_default](../../constants/font/family_default.md), [font.family_monospace](../../constants/font/family_monospace.md).
- **`text_formatting`** `series text_format` (optional) — The formatting of the displayed text. Formatting options support addition. For example, `text.format_bold + text.format_italic` will make the text both bold and italicized. Possible values: [text.format_none](https://www.tradingview.com/pine-script-reference/v6/#var_text.format_none), [text.format_bold](https://www.tradingview.com/pine-script-reference/v6/#var_text.format_bold), [text.format_italic](https://www.tradingview.com/pine-script-reference/v6/#var_text.format_italic). Optional. The default is [text.format_none](https://www.tradingview.com/pine-script-reference/v6/#var_text.format_none).

**Return type(s):** `void`

## Remarks

This function does not create the table itself, but defines the table’s cells. To use it, you first need to create a table object with [table.new()](./new.md).

Each [table.cell()](./cell.md) call overwrites all previously defined properties of a cell. If you call [table.cell()](./cell.md) twice in a row, e.g., the first time with text='Test Text', and the second time with text_color=[color.red](../../constants/color/red.md) but without a new text argument, the default value of the 'text' being an empty string, it will overwrite 'Test Text', and your cell will display an empty string. If you want, instead, to modify any of the cell's properties, use the table.cell_set_*() functions.

A single script can only display one table in each of the possible locations. If [table.cell()](./cell.md) is used on several bars to change the same attribute of a cell (e.g. change the background color of the cell to red on the first bar, then to yellow on the second bar), only the last change will be reflected in the table, i.e., the cell’s background will be yellow. Avoid unnecessary setting of cell properties by enclosing function calls in an [if](../../keywords/if.md) [barstate.islast](../../variables/barstate/islast.md) block whenever possible, to restrict their execution to the last bar of the series.

## See also

- [table.cell_set_bgcolor()](./cell_set_bgcolor.md)
- [table.cell_set_height()](./cell_set_height.md)
- [table.cell_set_text()](./cell_set_text.md)
- [table.cell_set_text_formatting()](./cell_set_text_formatting.md)
- [table.cell_set_text_color()](./cell_set_text_color.md)
- [table.cell_set_text_halign()](./cell_set_text_halign.md)
- [table.cell_set_text_size()](./cell_set_text_size.md)
- [table.cell_set_text_valign()](./cell_set_text_valign.md)
- [table.cell_set_width()](./cell_set_width.md)
- [table.cell_set_tooltip()](./cell_set_tooltip.md)
