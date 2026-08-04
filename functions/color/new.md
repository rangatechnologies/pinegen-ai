---
title: "color.new"
kind: function
namespace: color
source: https://www.tradingview.com/pine-script-reference/v6/#fun_color.new
---

# color.new

**Category:** Function

## Syntax

_4 overloaded forms:_

```pinescript
color.new(color, transp) → const color
```

```pinescript
color.new(color, transp) → series color
```

```pinescript
color.new(color, transp) → input color
```

```pinescript
color.new(color, transp) → simple color
```

## Description

Function color applies the specified transparency to the given color.

## Arguments

- **`color`** `const color` — Color to apply transparency to.
- **`transp`** `const int/float` — Possible values are from 0 (not transparent) to 100 (invisible).

## Returns

Color with specified transparency.

**Return type(s):** `const color`

## Remarks

Using arguments that are not constants (e.g., 'simple', 'input' or 'series') will have an impact on the colors displayed in the script's "Settings/Style" tab. See the [User Manual](https://www.tradingview.com/pine-script-docs/concepts/colors/#color-selection-through-script-settings) for more information.

## Examples

```pinescript
//@version=6
indicator("color.new", overlay=true)
plot(close, color=color.new(color.red, 50))
```
