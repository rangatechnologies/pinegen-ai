---
title: "fill"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_fill
---

# fill

**Category:** Function

## Syntax

_3 overloaded forms:_

```pinescript
fill(plot1, plot2, top_value, bottom_value, top_color, bottom_color, title, display, fillgaps, editable) → void
```

```pinescript
fill(hline1, hline2, color, title, editable, fillgaps, display) → void
```

```pinescript
fill(plot1, plot2, color, title, editable, show_last, fillgaps, display) → void
```

## Description

Fills background between two plots or hlines with a given color.

## Arguments

- **`plot1`** `plot` — The first plot object. Required argument.
- **`plot2`** `plot` — The second plot object. Required argument.
- **`top_value`** `series int/float` (optional) — Value where the gradient uses the `top_color`.
- **`bottom_value`** `series int/float` (optional) — Value where the gradient uses the `bottom_color`.
- **`top_color`** `series color` (optional) — Color of the gradient at the topmost value.
- **`bottom_color`** `series color` (optional) — Color of the gradient at the bottommost value.
- **`title`** `const string` (optional) — Title of the created fill object. Optional argument.
- **`display`** `input plot_simple_display` (optional) — Controls where the fill is displayed. Possible values are: [display.none](../constants/display/none.md), [display.all](../constants/display/all.md). Default is [display.all](../constants/display/all.md).
- **`fillgaps`** `const bool` (optional) — Controls continuing fills on gaps, i.e., when one of the plot() calls returns an na value. When true, the last fill will continue on gaps. The default is false.
- **`editable`** `input bool` (optional) — If true then fill style will be editable in Format dialog. Default is true.

**Return type(s):** `void`

## Detailed Description

Fill between two horizontal lines

```pinescript
//@version=6
indicator("Fill between hlines", overlay = false)
h1 = hline(20)
h2 = hline(10)
fill(h1, h2, color = color.new(color.blue, 90))
```

---

Fill between two plots

```pinescript
//@version=6
indicator("Fill between plots", overlay = true)
p1 = plot(open)
p2 = plot(close)
fill(p1, p2, color = color.new(color.green, 90))
```

---

Gradient fill between two horizontal lines

```pinescript
//@version=6
indicator("Gradient Fill between hlines", overlay = false)
topVal = input.int(100)
botVal = input.int(0)
topCol = input.color(color.red)
botCol = input.color(color.blue)
topLine = hline(100, color = topCol, linestyle = hline.style_solid)
botLine = hline(0,   color = botCol, linestyle = hline.style_solid)
fill(topLine, botLine, topVal, botVal, topCol, botCol)
```

## See also

- [plot()](./plot.md)
- [barcolor()](./barcolor.md)
- [bgcolor()](./bgcolor.md)
- [hline()](./hline.md)
- [color.new()](./color/new.md)
