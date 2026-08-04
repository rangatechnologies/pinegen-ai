---
title: "plotarrow"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_plotarrow
---

# plotarrow

**Category:** Function

## Syntax

```pinescript
plotarrow(series, title, colorup, colordown, offset, minheight, maxheight, editable, show_last, display, format, precision, force_overlay) → void
```

## Description

Plots up and down arrows on the chart. Up arrow is drawn at every indicator positive value, down arrow is drawn at every negative value. If indicator returns [na](../variables/na.md) then no arrow is drawn. Arrows has different height, the more absolute indicator value the longer arrow is drawn.

## Arguments

- **`series`** `series int/float` — Series of data to be plotted as arrows. Required argument.
- **`title`** `const string` (optional) — Title of the plot.
- **`colorup`** `series color` (optional) — Color of the up arrows. Optional argument.
- **`colordown`** `series color` (optional) — Color of the down arrows. Optional argument.
- **`offset`** `simple int` (optional) — Shifts arrows to the left or to the right on the given number of bars. Default is 0.
- **`minheight`** `input int` (optional) — Minimal possible arrow height in pixels. Default is 5.
- **`maxheight`** `input int` (optional) — Maximum possible arrow height in pixels. Default is 100.
- **`editable`** `input bool` (optional) — If true then plotarrow style will be editable in Format dialog. Default is true.
- **`show_last`** `input int` (optional) — Optional. The number of bars, counting backwards from the most recent bar, on which the function can draw.
- **`display`** `input plot_display` (optional) — Controls where the plot's information is displayed. Display options support addition and subtraction, meaning that using `display.all - display.status_line` will display the plot's information everywhere except in the script's status line. `display.price_scale + display.status_line` will display the plot only in the price scale and status line. When `display` arguments such as `display.price_scale` have user-controlled chart settings equivalents, the relevant plot information will only appear when all settings allow for it. Possible values: [display.none](../constants/display/none.md), [display.pane](../constants/display/pane.md), [display.data_window](../constants/display/data_window.md), [display.price_scale](../constants/display/price_scale.md), [display.status_line](../constants/display/status_line.md), [display.all](../constants/display/all.md). Optional. The default is [display.all](../constants/display/all.md).
- **`format`** `input string` (optional) — Determines whether the script formats the plot's values as prices, percentages, or volume values. The argument passed to this parameter supersedes the `format` parameter of the [indicator()](./indicator.md), and [strategy()](./strategy.md) functions. Optional. The default is the `format` value used by the [indicator()](./indicator.md)/[strategy()](./strategy.md) function. Possible values: [format.price](../constants/format/price.md), [format.percent](../constants/format/percent.md), [format.volume](../constants/format/volume.md).
- **`precision`** `input int` (optional) — The number of digits after the decimal point the plot's values show on the chart pane's y-axis, the script's status line, and the Data Window. Accepts a non-negative integer less than or equal to 16. The argument passed to this parameter supersedes the `precision` parameter of the [indicator()](./indicator.md) and [strategy()](./strategy.md) functions. When the function's `format` parameter uses [format.volume](../constants/format/volume.md), the `precision` parameter will not affect the result, as the decimal precision rules defined by [format.volume](../constants/format/volume.md) supersede other precision settings. Optional. The default is the `precision` value used by the [indicator()](./indicator.md)/[strategy()](./strategy.md) function.
- **`force_overlay`** `const bool` (optional) — If [true](../constants/true.md), the plotted results will display on the main chart pane, even when the script occupies a separate pane. Optional. The default is [false](../constants/false.md).

**Return type(s):** `void`

## Remarks

Use [plotarrow()](./plotarrow.md) function in conjunction with 'overlay=true' [indicator()](./indicator.md) parameter!

## Examples

```pinescript
//@version=6
indicator("plotarrow example", overlay=true)
codiff = close - open
plotarrow(codiff, colorup=color.new(color.teal,40), colordown=color.new(color.orange, 40))
```

## See also

- [plot()](./plot.md)
- [plotshape()](./plotshape.md)
- [plotchar()](./plotchar.md)
- [barcolor()](./barcolor.md)
- [bgcolor()](./bgcolor.md)
