---
title: "label.new"
kind: function
namespace: label
source: https://www.tradingview.com/pine-script-reference/v6/#fun_label.new
---

# label.new

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
label.new(point, text, xloc, yloc, color, style, textcolor, size, textalign, tooltip, text_font_family, force_overlay, text_formatting) → series label
```

```pinescript
label.new(x, y, text, xloc, yloc, color, style, textcolor, size, textalign, tooltip, text_font_family, force_overlay, text_formatting) → series label
```

## Description

Creates new label object.

## Arguments

- **`point`** `chart.point` — A [chart.point](../../types/chart/point.md) object that specifies the label's location.
- **`text`** `series string` (optional) — Label text. Default is empty string.
- **`xloc`** `series string` (optional) — See description of **x** argument. Possible values: [xloc.bar_index](../../constants/xloc/bar_index.md) and [xloc.bar_time](../../constants/xloc/bar_time.md). Default is [xloc.bar_index](../../constants/xloc/bar_index.md).
- **`yloc`** `series string` (optional) — Possible values are [yloc.price](../../constants/yloc/price.md), [yloc.abovebar](../../constants/yloc/abovebar.md), [yloc.belowbar](../../constants/yloc/belowbar.md). If yloc=[yloc.price](../../constants/yloc/price.md), **y** argument specifies the price of the label position. If yloc=[yloc.abovebar](../../constants/yloc/abovebar.md), label is located above bar. If yloc=[yloc.belowbar](../../constants/yloc/belowbar.md), label is located below bar. Default is [yloc.price](../../constants/yloc/price.md).
- **`color`** `series color` (optional) — Color of the label border and arrow
- **`style`** `series string` (optional) — Label style. Possible values: [label.style_none](../../constants/label/style_none.md), [label.style_xcross](../../constants/label/style_xcross.md), [label.style_cross](../../constants/label/style_cross.md), [label.style_triangleup](../../constants/label/style_triangleup.md), [label.style_triangledown](../../constants/label/style_triangledown.md), [label.style_flag](../../constants/label/style_flag.md), [label.style_circle](../../constants/label/style_circle.md), [label.style_arrowup](../../constants/label/style_arrowup.md), [label.style_arrowdown](../../constants/label/style_arrowdown.md), [label.style_label_up](../../constants/label/style_label_up.md), [label.style_label_down](../../constants/label/style_label_down.md), [label.style_label_left](../../constants/label/style_label_left.md), [label.style_label_right](../../constants/label/style_label_right.md), [label.style_label_lower_left](../../constants/label/style_label_lower_left.md), [label.style_label_lower_right](../../constants/label/style_label_lower_right.md), [label.style_label_upper_left](../../constants/label/style_label_upper_left.md), [label.style_label_upper_right](../../constants/label/style_label_upper_right.md), [label.style_label_center](../../constants/label/style_label_center.md), [label.style_square](../../constants/label/style_square.md), [label.style_diamond](../../constants/label/style_diamond.md), [label.style_text_outline](../../constants/label/style_text_outline.md). Default is [label.style_label_down](../../constants/label/style_label_down.md).
- **`textcolor`** `series color` (optional) — Text color.
- **`size`** `series int/string` (optional) — Optional. Size of the label. Accepts a positive [int](../../types/int.md) value or one of the built-in `size.*` constants. The constants and their equivalent numeric sizes are: [size.auto](../../constants/size/auto.md) (0), [size.tiny](../../constants/size/tiny.md) (\~7), [size.small](../../constants/size/small.md) (\~10), [size.normal](../../constants/size/normal.md) (12), [size.large](../../constants/size/large.md) (18), [size.huge](../../constants/size/huge.md) (24). The default value is [size.normal](../../constants/size/normal.md), which represents the numeric size of 12.
- **`textalign`** `series string` (optional) — Label text alignment. Possible values: [text.align_left](../../constants/text/align_left.md), [text.align_center](../../constants/text/align_center.md), [text.align_right](../../constants/text/align_right.md). Default value is [text.align_center](../../constants/text/align_center.md).
- **`tooltip`** `series string` (optional) — Hover to see tooltip label.
- **`text_font_family`** `series string` (optional) — The font family of the text. Optional. The default value is [font.family_default](../../constants/font/family_default.md). Possible values: [font.family_default](../../constants/font/family_default.md), [font.family_monospace](../../constants/font/family_monospace.md).
- **`force_overlay`** `const bool` (optional) — If [true](../../constants/true.md), the drawing will display on the main chart pane, even when the script occupies a separate pane. Optional. The default is [false](../../constants/false.md).
- **`text_formatting`** `series text_format` (optional) — The formatting of the displayed text. Formatting options support addition. For example, `text.format_bold + text.format_italic` will make the text both bold and italicized. Possible values: [text.format_none](https://www.tradingview.com/pine-script-reference/v6/#var_text.format_none), [text.format_bold](https://www.tradingview.com/pine-script-reference/v6/#var_text.format_bold), [text.format_italic](https://www.tradingview.com/pine-script-reference/v6/#var_text.format_italic). Optional. The default is [text.format_none](https://www.tradingview.com/pine-script-reference/v6/#var_text.format_none).

## Returns

Label ID object which may be passed to label.setXXX and label.getXXX functions.

**Return type(s):** `series label`

## Examples

```pinescript
//@version=6
indicator("label.new")
var label1 = label.new(bar_index, low, text="Hello, world!", style=label.style_circle)
label.set_x(label1, 0)
label.set_xloc(label1, time, xloc.bar_time)
label.set_color(label1, color.red)
label.set_size(label1, size.large)
```

## See also

- [label.delete()](./delete.md)
- [label.set_x()](./set_x.md)
- [label.set_y()](./set_y.md)
- [label.set_xy()](./set_xy.md)
- [label.set_xloc()](./set_xloc.md)
- [label.set_yloc()](./set_yloc.md)
- [label.set_color()](./set_color.md)
- [label.set_textcolor()](./set_textcolor.md)
- [label.set_style()](./set_style.md)
- [label.set_size()](./set_size.md)
- [label.set_textalign()](./set_textalign.md)
- [label.set_tooltip()](./set_tooltip.md)
- [label.set_text()](./set_text.md)
- [label.set_text_formatting()](./set_text_formatting.md)
