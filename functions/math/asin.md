---
title: "math.asin"
kind: function
namespace: math
source: https://www.tradingview.com/pine-script-reference/v6/#fun_math.asin
---

# math.asin

**Category:** Function

## Syntax

_4 overloaded forms:_

```pinescript
math.asin(angle) → simple float
```

```pinescript
math.asin(angle) → input float
```

```pinescript
math.asin(angle) → const float
```

```pinescript
math.asin(angle) → series float
```

## Description

The asin function returns the arcsine (in radians) of number such that sin(asin(y)) = y for y in range [-1, 1].

## Arguments

- **`angle`** `simple int/float` — The value, in radians, to use in the calculation.

## Returns

The arcsine of a value; the returned angle is in the range [-Pi/2, Pi/2], or [na](../../variables/na.md) if y is outside of range [-1, 1].

**Return type(s):** `simple float`
