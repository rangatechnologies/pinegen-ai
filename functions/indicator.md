---
title: "indicator"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_indicator
---

# indicator

**Category:** Function

## Syntax

```pinescript
indicator(title, shorttitle, overlay, format, precision, scale, max_bars_back, timeframe, timeframe_gaps, explicit_plot_zorder, max_lines_count, max_labels_count, max_boxes_count, calc_bars_count, max_polylines_count, dynamic_requests, behind_chart) → void
```

## Description

A declaration statement that identifies the script as an indicator and sets specific script-wide properties.

## Arguments

- **`title`** `const string` — A string representing the script's title. The script displays the string's text in all possible locations if the declaration statement does not include a `shorttitle` argument. Additionally, the "Publish script" window uses the text as the default title for a [script publication](https://www.tradingview.com/pine-script-docs/writing/publishing/).
- **`shorttitle`** `const string` (optional) — Optional. A string representing the script's display name on charts. If specified and not an empty string, the value's text replaces the `title` string in most chart locations, including the "Settings" window, the script's status line, the Data Window, and the "Create alert" dialog box. Otherwise, the `title` string appears as the script's title in all locations. The default is an empty string.
- **`overlay`** `const bool` (optional) — Optional. If `true`, the script's visuals appear on the main chart pane if the user adds it to the chart directly, or in another script's pane if the user applies it to that script. If `false`, the script's visuals appear in a separate pane. However, if a function call that creates [visuals](https://www.tradingview.com/pine-script-docs/visuals/overview/) includes `force_overlay = true`, its output always appears on the main chart pane, even if the script occupies a separate pane. Changes to this argument apply only after the user adds the script to the chart again. Additionally, if the user moves the script to another pane by selecting a "Move to" option in the script's "More" menu, the script does not move back to its original pane after any updates to the source code. The default is `false`.
- **`format`** `const string` (optional) — Optional. Specifies the format of the script's plotted values. Possible values are [format.inherit](../constants/format/inherit.md), [format.price](../constants/format/price.md), [format.volume](../constants/format/volume.md), and [format.percent](../constants/format/percent.md). The default is [format.inherit](../constants/format/inherit.md).
- **`precision`** `const int` (optional) — Optional. Specifies the number of fractional digits that the script shows for plotted numbers. The value must be an integer from 0 to 16. If specified and the `format` argument is [format.inherit](../constants/format/inherit.md), the script uses [format.price](../constants/format/price.md) as the formatting option instead. If the `format` argument is {format.volume}, the script ignores the `precision` value, because the decimal precision rules specified by [format.volume](../constants/format/volume.md) supersede other precision settings. By default, the script inherits the precision settings of the chart.
- **`scale`** `const scale_type` (optional) — Optional. Determines the location of the script's price scale and the scaling behavior of the script's visuals. Possible values are [scale.right](../constants/scale/right.md), [scale.left](../constants/scale/left.md), and [scale.none](../constants/scale/none.md). If specified and the script overlays on the main chart pane or another script's pane, the script scales its visuals independently to fit the pane's visual space. If the script occupies the same pane as the main chart or another script, [scale.right](../constants/scale/right.md) or [scale.left](../constants/scale/left.md) adds a separate price scale for the script to the left or right side of that pane. If the script occupies a separate pane, either argument positions the price scale for that pane on the left or right side without adding a new scale. If the argument is [scale.none](../constants/scale/none.md), which is valid only if the `overlay` argument is `true`, the script displays plotted numbers directly on the scale of the existing pane, or displays values on a new price scale if the user moves it to a new pane. Changes to the argument apply only after the user adds the script to the chart again. If not specified, the script uses the main price scale for the pane it occupies, and it does not scale its visuals separately if it overlays on an existing pane.
- **`max_bars_back`** `const int` (optional) — Optional. Sets the minimum length of all the script's historical buffers, which determine the number of bars back that the script can reference for each series using the [[]](../operators/history-reference.md) operator or the functions that retrieve history internally. The value must be an integer from 0 to 5000. By default, Pine's runtime system automatically calculates appropriate historical buffer sizes for each series while loading a script. Manually setting buffer sizes is necessary only in rare cases where automatic size detection fails. See the [Historical buffers](https://www.tradingview.com/pine-script-docs/language/execution-model/#historical-buffers) section of our User Manual for advanced details.
- **`timeframe`** `const string` (optional) — Optional. A valid [timeframe string](https://www.tradingview.com/pine-script-docs/concepts/timeframes/#timeframe-string-specifications) that determines the main timeframe the script uses for its calculations. If specified, the script automatically adds a "Timeframe" input to the "Settings/Inputs" tab. The input's displayed default in the tab represents the same timeframe as the specified argument. If the value is an empty string or not specified, the script uses the same timeframe as the chart. An argument is allowed for this parameter only if the script does not use [drawing types](https://www.tradingview.com/pine-script-docs/language/type-system/#drawing-types) or [alert()](./alert.md) function calls.
- **`timeframe_gaps`** `const bool` (optional) — Optional. Controls how the script displays plotted values if the `timeframe` value represents a higher timeframe than the chart's timeframe. An argument for this parameter is allowed only if the call includes a `timeframe` argument. If specified, the script adds a "Wait for timeframe closes" input, where users can change the setting, below the generated "Timeframe" input in the "Settings/Inputs" tab. If `true`, the indicator displays values only on the chart bars where new higher-timeframe data is available, and [na](../variables/na.md) on all other bars. If `false`, the indicator displays the last retrieved values on all chart bars where new data is not available. The default is `true`.
- **`explicit_plot_zorder`** `const bool` (optional) — Optional. Specifies which rules the script uses to determine the visual order of plots from `plot*()` calls, levels from [hline()](./hline.md) calls, and fills from [fill()](./fill.md) calls on the chart. If `true`, the indicator displays these visuals in the order of their function calls in the code. If `false`, the script uses the default [z-index](https://www.tradingview.com/pine-script-docs/visuals/overview/#z-index) rules to determine the order of the visuals. The default is `false`.
- **`max_lines_count`** `const int` (optional) — Optional. Determines the maximum number of [line](../types/line.md) objects that remain available to the script. The system automatically deletes the oldest [line](../types/line.md) objects when the number of lines exceeds the limit. The limit specified by the argument is approximate; the script might display more drawings than specified. The default is ~50 lines.
- **`max_labels_count`** `const int` (optional) — Optional. Determines the maximum number of [label](../types/label.md) objects that remain available to the script. The system automatically deletes the oldest [label](../types/label.md) objects when the number of labels exceeds the limit. The limit specified by the argument is approximate; the script might display more drawings than specified. The default is ~50 labels.
- **`max_boxes_count`** `const int` (optional) — Optional. Determines the maximum number of [box](../types/box.md) objects that remain available to the script. The system automatically deletes the oldest [box](../types/box.md) objects when the number of boxes exceeds the limit. The limit specified by the argument is approximate; the script might display more drawings than specified. The default is ~50 boxes.
- **`calc_bars_count`** `const int` (optional) — Optional. Determines how many of the most recent historical bars are available to the script. If specified, the script automatically adds a "Calculated bars" input to the "Settings/Inputs" tab. If the value is positive and less than the number of historical bars in the dataset, the script starts its calculations that number of bars before the most recent bar. If the value is 0, the script's calculations start on the dataset's first bar. The default is 0.
- **`max_polylines_count`** `const int` (optional) — Optional. Determines the maximum number of [polyline](../types/polyline.md) objects that remain available to the script. The system automatically deletes the oldest [polyline](../types/polyline.md) objects when the number of polylines exceeds the limit. The limit specified by the argument is approximate; the script might display more drawings than specified. The default is ~50 polylines.
- **`dynamic_requests`** `const bool` (optional) — Optional. Specifies whether the script can use dynamic `request.*()` function calls. Dynamic `request.*()` calls are allowed within the local scopes of conditional structures (e.g., [if](../keywords/if.md)), loops (e.g., [for](../keywords/for.md)), and exported functions. Additionally, such calls allow "series" arguments for several parameters that otherwise require values with "simple" or weaker qualifiers. See the [Dynamic requests](https://www.tradingview.com/pine-script-docs/concepts/other-timeframes-and-data/#dynamic-requests) section of our User Manual for more information. The default is `true`.
- **`behind_chart`** `const bool` (optional) — Optional. Controls whether all plots and drawings appear behind the chart display (if `true`) or in front of it (if `false`). This parameter takes effect only when the `overlay` argument is `true`. Changes to the argument apply only after the user adds the script to the chart again. The default is `true`.

**Return type(s):** `void`

## Remarks

Every indicator script must include exactly one [indicator()](./indicator.md) statement in the code.

## Examples

```pinescript
//@version=6
indicator("My script", shorttitle="Script")
plot(close)
```

## See also

- [strategy()](./strategy.md)
- [library()](./library.md)
