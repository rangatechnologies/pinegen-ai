---
title: "math.pow"
kind: function
namespace: math
source: https://www.tradingview.com/pine-script-reference/v6/#fun_math.pow
---

# math.pow

**Category:** Function

## Syntax

_4 overloaded forms:_

```pinescript
math.pow(base, exponent) → simple float
```

```pinescript
math.pow(base, exponent) → input float
```

```pinescript
math.pow(base, exponent) → const float
```

```pinescript
math.pow(base, exponent) → series float
```

## Description

Mathematical power function.

## Arguments

- **`base`** `simple int/float` — Specify the base to use.
- **`exponent`** `simple int/float` — Specifies the exponent.

## Returns

`base` raised to the power of `exponent`. If `base` is a series, it is calculated elementwise.

**Return type(s):** `simple float`

## Examples

```pinescript
//@version=6
indicator("math.pow", overlay=true)
plot(math.pow(close, 2))
```

## See also

- [math.sqrt()](./sqrt.md)
- [math.exp()](./exp.md)
