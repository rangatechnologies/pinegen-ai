---
title: "box.new"
kind: function
namespace: box
source: https://www.tradingview.com/pine-script-reference/v6/#fun_box.new
---

# box.new

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
box.new(top_left, bottom_right, border_color, border_width, border_style, extend, xloc, bgcolor, text, text_size, text_color, text_halign, text_valign, text_wrap, text_font_family, force_overlay, text_formatting) → series box
```

```pinescript
box.new(left, top, right, bottom, border_color, border_width, border_style, extend, xloc, bgcolor, text, text_size, text_color, text_halign, text_valign, text_wrap, text_font_family, force_overlay, text_formatting) → series box
```

## Description

Creates a new box object.

## Arguments

- **`top_left`** `chart.point` — A [chart.point](../../types/chart/point.md) object that specifies the top-left corner location of the box.
- **`bottom_right`** `chart.point` — A [chart.point](../../types/chart/point.md) object that specifies the bottom-right corner location of the box.
- **`border_color`** `series color` (optional) — Color of the four borders. Optional. The default is [color.blue](../../constants/color/blue.md).
- **`border_width`** `series int` (optional) — Width of the four borders, in pixels. Optional. The default is 1 pixel.
- **`border_style`** `series string` (optional) — Style of the four borders. Possible values: [line.style_solid](../../constants/line/style_solid.md), [line.style_dotted](../../constants/line/style_dotted.md), [line.style_dashed](../../constants/line/style_dashed.md). Optional. The default value is [line.style_solid](../../constants/line/style_solid.md).
- **`extend`** `series string` (optional) — When [extend.none](../../constants/extend/none.md) is used, the horizontal borders start at the left border and end at the right border. With [extend.left](../../constants/extend/left.md) or [extend.right](../../constants/extend/right.md), the horizontal borders are extended indefinitely to the left or right of the box, respectively. With [extend.both](../../constants/extend/both.md), the horizontal borders are extended on both sides. Optional. The default value is [extend.none](../../constants/extend/none.md).
- **`xloc`** `series string` (optional) — Determines whether the arguments to 'left' and 'right' are a bar index or a time value. If xloc = [xloc.bar_index](../../constants/xloc/bar_index.md), the arguments must be a bar index. If xloc = [xloc.bar_time](../../constants/xloc/bar_time.md), the arguments must be a UNIX time. Possible values: [xloc.bar_index](../../constants/xloc/bar_index.md) and [xloc.bar_time](../../constants/xloc/bar_time.md). Optional. The default is [xloc.bar_index](../../constants/xloc/bar_index.md).
- **`bgcolor`** `series color` (optional) — Background color of the box. Optional. The default is [color.blue](../../constants/color/blue.md).
- **`text`** `series string` (optional) — The text to be displayed inside the box. Optional. The default is empty string.
- **`text_size`** `series int/string` (optional) — Optional. Size of the box's text. The size can be any positive integer, or one of the `size.*` built-in constant strings. The constant strings and their equivalent integer values are: [size.auto](../../constants/size/auto.md) (0), [size.tiny](../../constants/size/tiny.md) (8), [size.small](../../constants/size/small.md) (10), [size.normal](../../constants/size/normal.md) (14), [size.large](../../constants/size/large.md) (20), [size.huge](../../constants/size/huge.md) (36). The default value is [size.auto](../../constants/size/auto.md) or 0.
- **`text_color`** `series color` (optional) — The color of the text. Optional. The default is [color.black](../../constants/color/black.md).
- **`text_halign`** `series string` (optional) — The horizontal alignment of the box's text. Optional. The default value is [text.align_center](../../constants/text/align_center.md). Possible values: [text.align_left](../../constants/text/align_left.md), [text.align_center](../../constants/text/align_center.md), [text.align_right](../../constants/text/align_right.md).
- **`text_valign`** `series string` (optional) — The vertical alignment of the box's text. Optional. The default value is [text.align_center](../../constants/text/align_center.md). Possible values: [text.align_top](../../constants/text/align_top.md), [text.align_center](../../constants/text/align_center.md), [text.align_bottom](../../constants/text/align_bottom.md).
- **`text_wrap`** `series string` (optional) — Optional. Whether to wrap text. Wrapped text starts a new line when it reaches the side of the box. Wrapped text lower than the bottom of the box is not displayed. Unwrapped text stays on a single line and *is displayed* past the width of the box if it is too long. If the `text_size` is 0 or [text.wrap_auto](../../constants/text/wrap_auto.md), this setting has no effect. The default value is [text.wrap_none](../../constants/text/wrap_none.md). Possible values: [text.wrap_none](../../constants/text/wrap_none.md), [text.wrap_auto](../../constants/text/wrap_auto.md).
- **`text_font_family`** `series string` (optional) — The font family of the text. Optional. The default value is [font.family_default](../../constants/font/family_default.md). Possible values: [font.family_default](../../constants/font/family_default.md), [font.family_monospace](../../constants/font/family_monospace.md).
- **`force_overlay`** `const bool` (optional) — If [true](../../constants/true.md), the drawing will display on the main chart pane, even when the script occupies a separate pane. Optional. The default is [false](../../constants/false.md).
- **`text_formatting`** `series text_format` (optional) — The formatting of the displayed text. Formatting options support addition. For example, `text.format_bold + text.format_italic` will make the text both bold and italicized. Possible values: [text.format_none](https://www.tradingview.com/pine-script-reference/v6/#var_text.format_none), [text.format_bold](https://www.tradingview.com/pine-script-reference/v6/#var_text.format_bold), [text.format_italic](https://www.tradingview.com/pine-script-reference/v6/#var_text.format_italic). Optional. The default is [text.format_none](https://www.tradingview.com/pine-script-reference/v6/#var_text.format_none).

## Returns

The ID of a box object which may be used in box.set_*() and box.get_*() functions.

**Return type(s):** `series box`

## Examples

```pinescript
//@version=6
indicator("box.new")
var b = box.new(time, open, time + 60 * 60 * 24, close, xloc=xloc.bar_time, border_style=line.style_dashed)
box.set_lefttop(b, time, 100)
box.set_rightbottom(b, time + 60 * 60 * 24, 500)
box.set_bgcolor(b, color.green)
```

## See also

- [box.delete()](./delete.md)
- [box.get_left()](./get_left.md)
- [box.get_top()](./get_top.md)
- [box.get_right()](./get_right.md)
- [box.get_bottom()](./get_bottom.md)
- [box.set_top_left_point()](./set_top_left_point.md)
- [box.set_left()](./set_left.md)
- [box.set_top()](./set_top.md)
- [box.set_bottom_right_point()](./set_bottom_right_point.md)
- [box.set_right()](./set_right.md)
- [box.set_bottom()](./set_bottom.md)
- [box.set_border_color()](./set_border_color.md)
- [box.set_bgcolor()](./set_bgcolor.md)
- [box.set_border_width()](./set_border_width.md)
- [box.set_border_style()](./set_border_style.md)
- [box.set_extend()](./set_extend.md)
- [box.set_text()](./set_text.md)
- [box.set_text_formatting()](./set_text_formatting.md)
- [box.set_xloc()](./set_xloc.md)
