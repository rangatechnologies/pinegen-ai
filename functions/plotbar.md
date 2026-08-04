---
title: "plotbar"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_plotbar
---

# plotbar

**Category:** Function

## Syntax

```pinescript
plotbar(open, high, low, close, title, color, editable, show_last, display, format, precision, force_overlay) → void
```

## Description

Plots ohlc bars on the chart.

## Arguments

- **`open`** `series int/float` — Open series of data to be used as open values of bars. Required argument.
- **`high`** `series int/float` — High series of data to be used as high values of bars. Required argument.
- **`low`** `series int/float` — Low series of data to be used as low values of bars. Required argument.
- **`close`** `series int/float` — Close series of data to be used as close values of bars. Required argument.
- **`title`** `const string` (optional) — Title of the plotbar. Optional argument.
- **`color`** `series color` (optional) — Color of the ohlc bars. You can use constants like 'color=color.red' or 'color=#ff001a' as well as complex expressions like 'color = close >= open ? color.green : color.red'. Optional argument.
- **`editable`** `input bool` (optional) — If true then plotbar style will be editable in Format dialog. Default is true.
- **`show_last`** `input int` (optional) — Optional. The number of bars, counting backwards from the most recent bar, on which the function can draw.
- **`display`** `input plot_display` (optional) — Controls where the plot's information is displayed. Display options support addition and subtraction, meaning that using `display.all - display.status_line` will display the plot's information everywhere except in the script's status line. `display.price_scale + display.status_line` will display the plot only in the price scale and status line. When `display` arguments such as `display.price_scale` have user-controlled chart settings equivalents, the relevant plot information will only appear when all settings allow for it. Possible values: [display.none](../constants/display/none.md), [display.pane](../constants/display/pane.md), [display.data_window](../constants/display/data_window.md), [display.price_scale](../constants/display/price_scale.md), [display.status_line](../constants/display/status_line.md), [display.all](../constants/display/all.md). Optional. The default is [display.all](../constants/display/all.md).
- **`format`** `input string` (optional) — Determines whether the script formats the plot's values as prices, percentages, or volume values. The argument passed to this parameter supersedes the `format` parameter of the [indicator()](./indicator.md), and [strategy()](./strategy.md) functions. Optional. The default is the `format` value used by the [indicator()](./indicator.md)/[strategy()](./strategy.md) function. Possible values: [format.price](../constants/format/price.md), [format.percent](../constants/format/percent.md), [format.volume](../constants/format/volume.md).
- **`precision`** `input int` (optional) — The number of digits after the decimal point the plot's values show on the chart pane's y-axis, the script's status line, and the Data Window. Accepts a non-negative integer less than or equal to 16. The argument passed to this parameter supersedes the `precision` parameter of the [indicator()](./indicator.md) and [strategy()](./strategy.md) functions. When the function's `format` parameter uses [format.volume](../constants/format/volume.md), the `precision` parameter will not affect the result, as the decimal precision rules defined by [format.volume](../constants/format/volume.md) supersede other precision settings. Optional. The default is the `precision` value used by the [indicator()](./indicator.md)/[strategy()](./strategy.md) function.
- **`force_overlay`** `const bool` (optional) — If [true](../constants/true.md), the plotted results will display on the main chart pane, even when the script occupies a separate pane. Optional. The default is [false](../constants/false.md).

**Return type(s):** `void`

## Remarks

Even if one value of open, high, low or close equal NaN then bar no draw.

The maximal value of open, high, low or close will be set as 'high', and the minimal value will be set as 'low'.

## Examples

```pinescript
//@version=6
indicator("plotbar example", overlay=true)
plotbar(open, high, low, close, title='Title', color = open < close ? color.green : color.red)
```

## See also

- [plotcandle()](./plotcandle.md)
