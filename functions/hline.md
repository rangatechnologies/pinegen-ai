---
title: "hline"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_hline
---

# hline

**Category:** Function

## Syntax

```pinescript
hline(price, title, color, linestyle, linewidth, editable, display) → hline
```

## Description

Renders a horizontal line at a given fixed price level.

## Arguments

- **`price`** `input int/float` — Price value at which the object will be rendered. Required argument.
- **`title`** `const string` (optional) — Title of the object.
- **`color`** `input color` (optional) — Color of the rendered line. Must be a constant value (not an expression). Optional argument.
- **`linestyle`** `input hline_style` (optional) — Style of the rendered line. Possible values are: [hline.style_solid](../constants/hline/style_solid.md), [hline.style_dotted](../constants/hline/style_dotted.md), [hline.style_dashed](../constants/hline/style_dashed.md). Optional argument.
- **`linewidth`** `input int` (optional) — Width of the rendered line. Default value is 1.
- **`editable`** `input bool` (optional) — If true then hline style will be editable in Format dialog. Default is true.
- **`display`** `input plot_simple_display` (optional) — Controls where the hline is displayed. Possible values are: [display.none](../constants/display/none.md), [display.all](../constants/display/all.md). Default is [display.all](../constants/display/all.md).

## Returns

An hline object, that can be used in [fill()](./fill.md)

**Return type(s):** `hline`

## Examples

```pinescript
//@version=6
indicator("input.hline", overlay=true)
hline(3.14, title='Pi', color=color.blue, linestyle=hline.style_dotted, linewidth=2)

// You may fill the background between any two hlines with a fill() function:
h1 = hline(20)
h2 = hline(10)
fill(h1, h2, color=color.new(color.green, 90))
```

## See also

- [fill()](./fill.md)
