---
title: "line.new"
kind: function
namespace: line
source: https://www.tradingview.com/pine-script-reference/v6/#fun_line.new
---

# line.new

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
line.new(x1, y1, x2, y2, xloc, extend, color, style, width, force_overlay) → series line
```

```pinescript
line.new(first_point, second_point, xloc, extend, color, style, width, force_overlay) → series line
```

## Description

Creates new line object.

## Arguments

- **`x1`** `series int` — Bar index (if xloc = [xloc.bar_index](../../constants/xloc/bar_index.md)) or bar UNIX time (if xloc = [xloc.bar_time](../../constants/xloc/bar_time.md)) of the first point of the line. Note that objects positioned using [xloc.bar_index](../../constants/xloc/bar_index.md) cannot be drawn further than 500 bars into the future.
- **`y1`** `series int/float` — Price of the first point of the line.
- **`x2`** `series int` — Bar index (if xloc = [xloc.bar_index](../../constants/xloc/bar_index.md)) or bar UNIX time (if xloc = [xloc.bar_time](../../constants/xloc/bar_time.md)) of the second point of the line. Note that objects positioned using [xloc.bar_index](../../constants/xloc/bar_index.md) cannot be drawn further than 500 bars into the future.
- **`y2`** `series int/float` — Price of the second point of the line.
- **`xloc`** `series string` (optional) — See description of **x1** argument. Possible values: [xloc.bar_index](../../constants/xloc/bar_index.md) and [xloc.bar_time](../../constants/xloc/bar_time.md). Default is [xloc.bar_index](../../constants/xloc/bar_index.md).
- **`extend`** `series string` (optional) — If extend=[extend.none](../../constants/extend/none.md), draws segment starting at point (x1, y1) and ending at point (x2, y2). If extend is equal to [extend.right](../../constants/extend/right.md) or [extend.left](../../constants/extend/left.md), draws a ray starting at point (x1, y1) or (x2, y2), respectively. If extend=[extend.both](../../constants/extend/both.md), draws a straight line that goes through these points. Default value is [extend.none](../../constants/extend/none.md).
- **`color`** `series color` (optional) — Line color.
- **`style`** `series string` (optional) — Line style. Possible values: [line.style_solid](../../constants/line/style_solid.md), [line.style_dotted](../../constants/line/style_dotted.md), [line.style_dashed](../../constants/line/style_dashed.md), [line.style_arrow_left](../../constants/line/style_arrow_left.md), [line.style_arrow_right](../../constants/line/style_arrow_right.md), [line.style_arrow_both](../../constants/line/style_arrow_both.md).
- **`width`** `series int` (optional) — Line width in pixels.
- **`force_overlay`** `const bool` (optional) — If [true](../../constants/true.md), the drawing will display on the main chart pane, even when the script occupies a separate pane. Optional. The default is [false](../../constants/false.md).

## Returns

Line ID object which may be passed to line.setXXX and line.getXXX functions.

**Return type(s):** `series line`

## Examples

```pinescript
//@version=6
indicator("line.new")
var line1 = line.new(0, low, bar_index, high, extend=extend.right)
var line2 = line.new(time, open, time + 60 * 60 * 24, close, xloc=xloc.bar_time, style=line.style_dashed)
line.set_x2(line1, 0)
line.set_xloc(line1, time, time + 60 * 60 * 24, xloc.bar_time)
line.set_color(line2, color.green)
line.set_width(line2, 5)
```

## See also

- [line.delete()](./delete.md)
- [line.set_x1()](./set_x1.md)
- [line.set_y1()](./set_y1.md)
- [line.set_xy1()](./set_xy1.md)
- [line.set_x2()](./set_x2.md)
- [line.set_y2()](./set_y2.md)
- [line.set_xy2()](./set_xy2.md)
- [line.set_xloc()](./set_xloc.md)
- [line.set_color()](./set_color.md)
- [line.set_extend()](./set_extend.md)
- [line.set_style()](./set_style.md)
- [line.set_width()](./set_width.md)
