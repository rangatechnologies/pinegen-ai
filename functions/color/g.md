---
title: "color.g"
kind: function
namespace: color
source: https://www.tradingview.com/pine-script-reference/v6/#fun_color.g
---

# color.g

**Category:** Function

## Syntax

_4 overloaded forms:_

```pinescript
color.g(color) → series float
```

```pinescript
color.g(color) → const float
```

```pinescript
color.g(color) → input float
```

```pinescript
color.g(color) → simple float
```

## Description

Retrieves the value of the color's green component.

## Arguments

- **`color`** `series color` — Color.

## Returns

The value (0 to 255) of the color's green component.

**Return type(s):** `series float`

## Examples

```pinescript
//@version=6
indicator("color.g", overlay=true)
plot(color.g(color.green))
```
