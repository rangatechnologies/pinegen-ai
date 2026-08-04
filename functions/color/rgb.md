---
title: "color.rgb"
kind: function
namespace: color
source: https://www.tradingview.com/pine-script-reference/v6/#fun_color.rgb
---

# color.rgb

**Category:** Function

## Syntax

_4 overloaded forms:_

```pinescript
color.rgb(red, green, blue, transp) → series color
```

```pinescript
color.rgb(red, green, blue, transp) → const color
```

```pinescript
color.rgb(red, green, blue, transp) → input color
```

```pinescript
color.rgb(red, green, blue, transp) → simple color
```

## Description

Creates a new color with transparency using the RGB color model.

## Arguments

- **`red`** `series int/float` — Red color component. Possible values are from 0 to 255.
- **`green`** `series int/float` — Green color component. Possible values are from 0 to 255.
- **`blue`** `series int/float` — Blue color component. Possible values are from 0 to 255.
- **`transp`** `series int/float` (optional) — Optional. Color transparency. Possible values are from 0 (opaque) to 100 (invisible). Default value is 0.

## Returns

Color with specified transparency.

**Return type(s):** `series color`

## Remarks

Using arguments that are not constants (e.g., 'simple', 'input' or 'series') will have an impact on the colors displayed in the script's "Settings/Style" tab. See the [User Manual](https://www.tradingview.com/pine-script-docs/concepts/colors/#color-selection-through-script-settings) for more information.

## Examples

```pinescript
//@version=6
indicator("color.rgb", overlay=true)
plot(close, color=color.rgb(255, 0, 0, 50))
```
