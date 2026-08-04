---
title: "math.acos"
kind: function
namespace: math
source: https://www.tradingview.com/pine-script-reference/v6/#fun_math.acos
---

# math.acos

**Category:** Function

## Syntax

_4 overloaded forms:_

```pinescript
math.acos(angle) → simple float
```

```pinescript
math.acos(angle) → input float
```

```pinescript
math.acos(angle) → const float
```

```pinescript
math.acos(angle) → series float
```

## Description

The acos function returns the arccosine (in radians) of number such that cos(acos(y)) = y for y in range [-1, 1].

## Arguments

- **`angle`** `simple int/float` — The value, in radians, to use in the calculation.

## Returns

The arc cosine of a value; the returned angle is in the range [0, Pi], or [na](../../variables/na.md) if y is outside of range [-1, 1].

**Return type(s):** `simple float`
