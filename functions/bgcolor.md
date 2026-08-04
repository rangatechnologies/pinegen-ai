---
title: "bgcolor"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_bgcolor
---

# bgcolor

**Category:** Function

## Syntax

```pinescript
bgcolor(color, offset, editable, show_last, title, display, force_overlay) → void
```

## Description

Fill background of bars with specified color.

## Arguments

- **`color`** `series color` — Color of the filled background. You can use constants like 'red' or '#ff001a' as well as complex expressions like 'close >= open ? color.green : color.red'. Required argument.
- **`offset`** `simple int` (optional) — Shifts the color series to the left or to the right on the given number of bars. Default is 0.
- **`editable`** `input bool` (optional) — If true then bgcolor style will be editable in Format dialog. Default is true.
- **`show_last`** `input int` (optional) — Optional. The number of bars, counting backwards from the most recent bar, on which the function can draw.
- **`title`** `const string` (optional) — Title of the bgcolor. Optional argument.
- **`display`** `input plot_simple_display` (optional) — Controls where the bgcolor is displayed. Possible values are: [display.none](../constants/display/none.md), [display.all](../constants/display/all.md). Default is [display.all](../constants/display/all.md).
- **`force_overlay`** `const bool` (optional) — If [true](../constants/true.md), the plotted results will display on the main chart pane, even when the script occupies a separate pane. Optional. The default is [false](../constants/false.md).

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
indicator("bgcolor example", overlay=true)
bgcolor(close < open ? color.new(color.red,70) : color.new(color.green, 70))
```

## See also

- [barcolor()](./barcolor.md)
- [plot()](./plot.md)
- [fill()](./fill.md)
