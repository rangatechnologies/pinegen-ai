---
title: "plot"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_plot
---

# plot

**Category:** Function

## Syntax

```pinescript
plot(series, title, color, linewidth, style, trackprice, histbase, offset, join, editable, show_last, display, format, precision, force_overlay, linestyle) → plot
```

## Description

Plots a series of data on the chart.

## Arguments

- **`series`** `series int/float` — Series of data to be plotted. Required argument.
- **`title`** `const string` (optional) — Title of the plot.
- **`color`** `series color` (optional) — Color of the plot. You can use constants like 'color=color.red' or 'color=#ff001a' as well as complex expressions like 'color = close >= open ? color.green : color.red'. Optional argument.
- **`linewidth`** `input int` (optional) — Width of the plotted line. Default value is 1. Not applicable to every style.
- **`style`** `input plot_style` (optional) — Type of plot. Possible values are: [plot.style_line](../constants/plot/style_line.md), [plot.style_stepline](../constants/plot/style_stepline.md), [plot.style_stepline_diamond](../constants/plot/style_stepline_diamond.md), [plot.style_histogram](../constants/plot/style_histogram.md), [plot.style_cross](../constants/plot/style_cross.md), [plot.style_area](../constants/plot/style_area.md), [plot.style_columns](../constants/plot/style_columns.md), [plot.style_circles](../constants/plot/style_circles.md), [plot.style_linebr](../constants/plot/style_linebr.md), [plot.style_areabr](../constants/plot/style_areabr.md), [plot.style_steplinebr](../constants/plot/style_steplinebr.md). Default value is [plot.style_line](../constants/plot/style_line.md).
- **`trackprice`** `input bool` (optional) — If true then a horizontal price line will be shown at the level of the last indicator value. Default is false.
- **`histbase`** `input int/float` (optional) — The price value used as the reference level when rendering plot with [plot.style_histogram](../constants/plot/style_histogram.md), [plot.style_columns](../constants/plot/style_columns.md) or [plot.style_area](../constants/plot/style_area.md) style. Default is 0.0.
- **`offset`** `simple int` (optional) — Shifts the plot to the left or to the right on the given number of bars. Default is 0.
- **`join`** `input bool` (optional) — If true then plot points will be joined with line, applicable only to [plot.style_cross](../constants/plot/style_cross.md) and [plot.style_circles](../constants/plot/style_circles.md) styles. Default is false.
- **`editable`** `input bool` (optional) — If true then plot style will be editable in Format dialog. Default is true.
- **`show_last`** `input int` (optional) — Optional. The number of bars, counting backwards from the most recent bar, on which the function can draw.
- **`display`** `input plot_display` (optional) — Controls where the plot's information is displayed. Display options support addition and subtraction, meaning that using `display.all - display.status_line` will display the plot's information everywhere except in the script's status line. `display.price_scale + display.status_line` will display the plot only in the price scale and status line. When `display` arguments such as `display.price_scale` have user-controlled chart settings equivalents, the relevant plot information will only appear when all settings allow for it. Possible values: [display.none](../constants/display/none.md), [display.pane](../constants/display/pane.md), [display.data_window](../constants/display/data_window.md), [display.price_scale](../constants/display/price_scale.md), [display.status_line](../constants/display/status_line.md), [display.all](../constants/display/all.md). Optional. The default is [display.all](../constants/display/all.md).
- **`format`** `input string` (optional) — Determines whether the script formats the plot's values as prices, percentages, or volume values. The argument passed to this parameter supersedes the `format` parameter of the [indicator()](./indicator.md), and [strategy()](./strategy.md) functions. Optional. The default is the `format` value used by the [indicator()](./indicator.md)/[strategy()](./strategy.md) function. Possible values: [format.price](../constants/format/price.md), [format.percent](../constants/format/percent.md), [format.volume](../constants/format/volume.md).
- **`precision`** `input int` (optional) — The number of digits after the decimal point the plot's values show on the chart pane's y-axis, the script's status line, and the Data Window. Accepts a non-negative integer less than or equal to 16. The argument passed to this parameter supersedes the `precision` parameter of the [indicator()](./indicator.md) and [strategy()](./strategy.md) functions. When the function's `format` parameter uses [format.volume](../constants/format/volume.md), the `precision` parameter will not affect the result, as the decimal precision rules defined by [format.volume](../constants/format/volume.md) supersede other precision settings. Optional. The default is the `precision` value used by the [indicator()](./indicator.md)/[strategy()](./strategy.md) function.
- **`force_overlay`** `const bool` (optional) — If [true](../constants/true.md), the plotted results will display on the main chart pane, even when the script occupies a separate pane. Optional. The default is [false](../constants/false.md).
- **`linestyle`** `input plot_line_style` (optional) — Optional. A modifier for plot styles that display lines. It specifies whether the plotted line is solid ([plot.linestyle_solid](../constants/plot/linestyle_solid.md)), dashed ([plot.linestyle_dashed](../constants/plot/linestyle_dashed.md)), or dotted ([plot.linestyle_dotted](../constants/plot/linestyle_dotted.md)). The modifier applies only when the function uses one of the following `style` arguments: [plot.style_line](../constants/plot/style_line.md), [plot.style_linebr](../constants/plot/style_linebr.md), [plot.style_stepline](../constants/plot/style_stepline.md), [plot.style_stepline_diamond](../constants/plot/style_stepline_diamond.md), and [plot.style_area](../constants/plot/style_area.md). The default is [plot.linestyle_solid](../constants/plot/linestyle_solid.md).

## Returns

A plot object, that can be used in [fill()](./fill.md)

**Return type(s):** `plot`

## Examples

```pinescript
//@version=6
indicator("plot")
plot(high+low, title='Title', color=color.new(#00ffaa, 70), linewidth=2, style=plot.style_area, offset=15, trackprice=true)

// You may fill the background between any two plots with a fill() function:
p1 = plot(open)
p2 = plot(close)
fill(p1, p2, color=color.new(color.green, 90))
```

## See also

- [plotshape()](./plotshape.md)
- [plotchar()](./plotchar.md)
- [plotarrow()](./plotarrow.md)
- [barcolor()](./barcolor.md)
- [bgcolor()](./bgcolor.md)
- [fill()](./fill.md)
