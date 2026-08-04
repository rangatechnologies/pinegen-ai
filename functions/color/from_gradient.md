---
title: "color.from_gradient"
kind: function
namespace: color
source: https://www.tradingview.com/pine-script-reference/v6/#fun_color.from_gradient
---

# color.from_gradient

**Category:** Function

## Syntax

```pinescript
color.from_gradient(value, bottom_value, top_value, bottom_color, top_color) → series color
```

## Description

Based on the relative position of value in the bottom_value to top_value range, the function returns a color from the gradient defined by bottom_color to top_color.

## Arguments

- **`value`** `series int/float` — Value to calculate the position-dependent color.
- **`bottom_value`** `series int/float` — Bottom position value corresponding to bottom_color.
- **`top_value`** `series int/float` — Top position value corresponding to top_color.
- **`bottom_color`** `series color` — Bottom position color.
- **`top_color`** `series color` — Top position color.

## Returns

A color calculated from the linear gradient between bottom_color to top_color.

**Return type(s):** `series color`

## Remarks

Using this function will have an impact on the colors displayed in the script's "Settings/Style" tab. See the [User Manual](https://www.tradingview.com/pine-script-docs/concepts/colors/#color-selection-through-script-settings) for more information.

## Examples

```pinescript
//@version=6
indicator("color.from_gradient", overlay=true)
color1 = color.from_gradient(close, low, high, color.yellow, color.lime)
color2 = color.from_gradient(ta.rsi(close, 7), 0, 100, color.rgb(255, 0, 0), color.rgb(0, 255, 0, 50))
plot(close, color=color1)
plot(ta.rsi(close,7), color=color2)
```
