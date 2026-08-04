---
title: "color.t"
kind: function
namespace: color
source: https://www.tradingview.com/pine-script-reference/v6/#fun_color.t
---

# color.t

**Category:** Function

## Syntax

_4 overloaded forms:_

```pinescript
color.t(color) → series float
```

```pinescript
color.t(color) → const float
```

```pinescript
color.t(color) → input float
```

```pinescript
color.t(color) → simple float
```

## Description

Retrieves the color's transparency.

## Arguments

- **`color`** `series color` — Color.

## Returns

The value (0-100) of the color's transparency.

**Return type(s):** `series float`

## Examples

```pinescript
//@version=6
indicator("color.t", overlay=true)
plot(color.t(color.new(color.red, 50)))
```
