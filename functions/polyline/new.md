---
title: "polyline.new"
kind: function
namespace: polyline
source: https://www.tradingview.com/pine-script-reference/v6/#fun_polyline.new
---

# polyline.new

**Category:** Function

## Syntax

```pinescript
polyline.new(points, curved, closed, xloc, line_color, fill_color, line_style, line_width, force_overlay) → series polyline
```

## Description

Creates a new [polyline](../../types/polyline.md) instance and displays it on the chart, sequentially connecting all of the points in the `points` array with line segments. The segments in the drawing can be straight or curved depending on the `curved` parameter.

## Arguments

- **`points`** `array<chart.point>` — An array of [chart.point](../../types/chart/point.md) objects for the drawing to sequentially connect.
- **`curved`** `series bool` (optional) — If [true](../../constants/true.md), the drawing will connect all points from the `points` array using curved line segments. Optional. The default is [false](../../constants/false.md).
- **`closed`** `series bool` (optional) — If [true](../../constants/true.md), the drawing will also connect the first point to the last point from the `points` array, resulting in a closed polyline. Optional. The default is [false](../../constants/false.md).
- **`xloc`** `series string` (optional) — Determines the field of the [chart.point](../../types/chart/point.md) objects in the `points` array that the polyline will use for its x-coordinates. If [xloc.bar_index](../../constants/xloc/bar_index.md), the polyline will use the `index` field from each point. If [xloc.bar_time](../../constants/xloc/bar_time.md), it will use the `time` field. Optional. The default is [xloc.bar_index](../../constants/xloc/bar_index.md).
- **`line_color`** `series color` (optional) — The color of the line segments. Optional. The default is [color.blue](../../constants/color/blue.md).
- **`fill_color`** `series color` (optional) — The fill color of the polyline. Optional. The default is [na](../../variables/na.md).
- **`line_style`** `series string` (optional) — The style of the polyline. Possible values: [line.style_solid](../../constants/line/style_solid.md), [line.style_dotted](../../constants/line/style_dotted.md), [line.style_dashed](../../constants/line/style_dashed.md), [line.style_arrow_left](../../constants/line/style_arrow_left.md), [line.style_arrow_right](../../constants/line/style_arrow_right.md), [line.style_arrow_both](../../constants/line/style_arrow_both.md). Optional. The default is [line.style_solid](../../constants/line/style_solid.md).
- **`line_width`** `series int` (optional) — The width of the line segments, expressed in pixels. Optional. The default is 1.
- **`force_overlay`** `const bool` (optional) — If [true](../../constants/true.md), the drawing will display on the main chart pane, even when the script occupies a separate pane. Optional. The default is [false](../../constants/false.md).

## Returns

The ID of a new polyline object that a script can use in other `polyline.*()` functions.

**Return type(s):** `series polyline`

## Examples

```pinescript
//@version=6
indicator("Polylines example", overlay = true)

//@variable If `true`, connects all points in the polyline with curved line segments.
bool curvedInput = input.bool(false, "Curve Polyline")
//@variable If `true`, connects the first point in the polyline to the last point.
bool closedInput = input.bool(true, "Close Polyline")
//@variable The color of the space filled by the polyline.
color fillcolor = input.color(color.new(color.blue, 90), "Fill Color")

// Time and price inputs for the polyline's points.
p1x = input.time(0,  "p1", confirm = true, inline = "p1")
p1y = input.price(0, "  ", confirm = true, inline = "p1")
p2x = input.time(0,  "p2", confirm = true, inline = "p2")
p2y = input.price(0, "  ", confirm = true, inline = "p2")
p3x = input.time(0,  "p3", confirm = true, inline = "p3")
p3y = input.price(0, "  ", confirm = true, inline = "p3")
p4x = input.time(0,  "p4", confirm = true, inline = "p4")
p4y = input.price(0, "  ", confirm = true, inline = "p4")
p5x = input.time(0,  "p5", confirm = true, inline = "p5")
p5y = input.price(0, "  ", confirm = true, inline = "p5")

if barstate.islastconfirmedhistory
	//@variable An array of `chart.point` objects for the new polyline.
	var points = array.new<chart.point>()
	// Push new `chart.point` instances into the `points` array.
	points.push(chart.point.from_time(p1x, p1y))
	points.push(chart.point.from_time(p2x, p2y))
	points.push(chart.point.from_time(p3x, p3y))
	points.push(chart.point.from_time(p4x, p4y))
	points.push(chart.point.from_time(p5x, p5y))
	// Add labels for each `chart.point` in `points`.
	l1p1 = label.new(points.get(0), text = "p1", xloc = xloc.bar_time, color = na)
	l1p2 = label.new(points.get(1), text = "p2", xloc = xloc.bar_time, color = na)
	l2p1 = label.new(points.get(2), text = "p3", xloc = xloc.bar_time, color = na)
	l2p2 = label.new(points.get(3), text = "p4", xloc = xloc.bar_time, color = na)
	// Create a new polyline that connects each `chart.point` in the `points` array, starting from the first.
	polyline.new(points, curved = curvedInput, closed = closedInput, fill_color = fillcolor, xloc = xloc.bar_time)
```

## See also

- [chart.point.new()](../chart/point.new.md)
