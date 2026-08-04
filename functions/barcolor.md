---
title: "barcolor"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_barcolor
---

# barcolor

**Category:** Function

## Syntax

```pinescript
barcolor(color, offset, editable, show_last, title, display) → void
```

## Description

Set color of bars.

## Arguments

- **`color`** `series color` — Color of bars. You can use constants like 'red' or '#ff001a' as well as complex expressions like 'close >= open ? color.green : color.red'. Required argument.
- **`offset`** `simple int` (optional) — Shifts the color series to the left or to the right on the given number of bars. Default is 0.
- **`editable`** `input bool` (optional) — If true then barcolor style will be editable in Format dialog. Default is true.
- **`show_last`** `input int` (optional) — Optional. The number of bars, counting backwards from the most recent bar, on which the function can draw.
- **`title`** `const string` (optional) — Title of the barcolor. Optional argument.
- **`display`** `input plot_simple_display` (optional) — Controls where the barcolor is displayed. Possible values are: [display.none](../constants/display/none.md), [display.all](../constants/display/all.md). Default is [display.all](../constants/display/all.md).

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
indicator("barcolor example", overlay=true)
barcolor(close < open ? color.black : color.white)
```

## See also

- [bgcolor()](./bgcolor.md)
- [plot()](./plot.md)
- [fill()](./fill.md)
