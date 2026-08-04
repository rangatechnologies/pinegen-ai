---
title: "color.r"
kind: function
namespace: color
source: https://www.tradingview.com/pine-script-reference/v6/#fun_color.r
---

# color.r

**Category:** Function

## Syntax

_4 overloaded forms:_

```pinescript
color.r(color) → series float
```

```pinescript
color.r(color) → const float
```

```pinescript
color.r(color) → input float
```

```pinescript
color.r(color) → simple float
```

## Description

Retrieves the value of the color's red component.

## Arguments

- **`color`** `series color` — Color.

## Returns

The value (0 to 255) of the color's red component.

**Return type(s):** `series float`

## Examples

```pinescript
//@version=6
indicator("color.r", overlay=true)
plot(color.r(color.red))
```
