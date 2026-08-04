---
title: "color.b"
kind: function
namespace: color
source: https://www.tradingview.com/pine-script-reference/v6/#fun_color.b
---

# color.b

**Category:** Function

## Syntax

_4 overloaded forms:_

```pinescript
color.b(color) → series float
```

```pinescript
color.b(color) → const float
```

```pinescript
color.b(color) → input float
```

```pinescript
color.b(color) → simple float
```

## Description

Retrieves the value of the color's blue component.

## Arguments

- **`color`** `series color` — Color.

## Returns

The value (0 to 255) of the color's blue component.

**Return type(s):** `series float`

## Examples

```pinescript
//@version=6
indicator("color.b", overlay=true)
plot(color.b(color.blue))
```
