---
title: "plotshape"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_plotshape
---

# plotshape

**Category:** Function

## Syntax

```pinescript
plotshape(series, title, style, location, color, offset, text, textcolor, editable, size, show_last, display, format, precision, force_overlay) → void
```

## Description

Plots visual shapes on the chart.

## Arguments

- **`series`** `series int/float/bool` — Series of data to be plotted as shapes. Series is treated as a series of boolean values for all location values except [location.absolute](../constants/location/absolute.md). Required argument.
- **`title`** `const string` (optional) — Title of the plot.
- **`style`** `input string` (optional) — Type of plot. Possible values are: [shape.xcross](../constants/shape/xcross.md), [shape.cross](../constants/shape/cross.md), [shape.triangleup](../constants/shape/triangleup.md), [shape.triangledown](../constants/shape/triangledown.md), [shape.flag](../constants/shape/flag.md), [shape.circle](../constants/shape/circle.md), [shape.arrowup](../constants/shape/arrowup.md), [shape.arrowdown](../constants/shape/arrowdown.md), [shape.labelup](../constants/shape/labelup.md), [shape.labeldown](../constants/shape/labeldown.md), [shape.square](../constants/shape/square.md), [shape.diamond](../constants/shape/diamond.md). Default value is [shape.xcross](../constants/shape/xcross.md).
- **`location`** `input string` (optional) — Location of shapes on the chart. Possible values are: [location.abovebar](../constants/location/abovebar.md), [location.belowbar](../constants/location/belowbar.md), [location.top](../constants/location/top.md), [location.bottom](../constants/location/bottom.md), [location.absolute](../constants/location/absolute.md). Default value is [location.abovebar](../constants/location/abovebar.md).
- **`color`** `series color` (optional) — Color of the shapes. You can use constants like 'color=color.red' or 'color=#ff001a' as well as complex expressions like 'color = close >= open ? color.green : color.red'. Optional argument.
- **`offset`** `simple int` (optional) — Shifts shapes to the left or to the right on the given number of bars. Default is 0.
- **`text`** `const string` (optional) — Text to display with the shape. You can use multiline text, to separate lines use '\n' escape sequence. Example: 'line one\nline two'.
- **`textcolor`** `series color` (optional) — Color of the text. You can use constants like 'textcolor=color.red' or 'textcolor=#ff001a' as well as complex expressions like 'textcolor = close >= open ? color.green : color.red'. Optional argument.
- **`editable`** `input bool` (optional) — If true then plotshape style will be editable in Format dialog. Default is true.
- **`size`** `const string` (optional) — Size of shapes on the chart. Possible values are: [size.auto](../constants/size/auto.md), [size.tiny](../constants/size/tiny.md), [size.small](../constants/size/small.md), [size.normal](../constants/size/normal.md), [size.large](../constants/size/large.md), [size.huge](../constants/size/huge.md). Default is [size.auto](../constants/size/auto.md).
- **`show_last`** `input int` (optional) — Optional. The number of bars, counting backwards from the most recent bar, on which the function can draw.
- **`display`** `input plot_display` (optional) — Controls where the plot's information is displayed. Display options support addition and subtraction, meaning that using `display.all - display.status_line` will display the plot's information everywhere except in the script's status line. `display.price_scale + display.status_line` will display the plot only in the price scale and status line. When `display` arguments such as `display.price_scale` have user-controlled chart settings equivalents, the relevant plot information will only appear when all settings allow for it. Possible values: [display.none](../constants/display/none.md), [display.pane](../constants/display/pane.md), [display.data_window](../constants/display/data_window.md), [display.price_scale](../constants/display/price_scale.md), [display.status_line](../constants/display/status_line.md), [display.all](../constants/display/all.md). Optional. The default is [display.all](../constants/display/all.md).
- **`format`** `input string` (optional) — Determines whether the script formats the plot's values as prices, percentages, or volume values. The argument passed to this parameter supersedes the `format` parameter of the [indicator()](./indicator.md), and [strategy()](./strategy.md) functions. Optional. The default is the `format` value used by the [indicator()](./indicator.md)/[strategy()](./strategy.md) function. Possible values: [format.price](../constants/format/price.md), [format.percent](../constants/format/percent.md), [format.volume](../constants/format/volume.md).
- **`precision`** `input int` (optional) — The number of digits after the decimal point the plot's values show on the chart pane's y-axis, the script's status line, and the Data Window. Accepts a non-negative integer less than or equal to 16. The argument passed to this parameter supersedes the `precision` parameter of the [indicator()](./indicator.md) and [strategy()](./strategy.md) functions. When the function's `format` parameter uses [format.volume](../constants/format/volume.md), the `precision` parameter will not affect the result, as the decimal precision rules defined by [format.volume](../constants/format/volume.md) supersede other precision settings. Optional. The default is the `precision` value used by the [indicator()](./indicator.md)/[strategy()](./strategy.md) function.
- **`force_overlay`** `const bool` (optional) — If [true](../constants/true.md), the plotted results will display on the main chart pane, even when the script occupies a separate pane. Optional. The default is [false](../constants/false.md).

**Return type(s):** `void`

## Remarks

Use [plotshape()](./plotshape.md) function in conjunction with 'overlay=true' [indicator()](./indicator.md) parameter!

## Examples

```pinescript
//@version=6
indicator("plotshape example 1", overlay=true)
data = close >= open
plotshape(data, style=shape.xcross)
```

## See also

- [plot()](./plot.md)
- [plotchar()](./plotchar.md)
- [plotarrow()](./plotarrow.md)
- [barcolor()](./barcolor.md)
- [bgcolor()](./bgcolor.md)
