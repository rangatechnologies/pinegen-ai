---
title: "math.max"
kind: function
namespace: math
source: https://www.tradingview.com/pine-script-reference/v6/#fun_math.max
---

# math.max

**Category:** Function

## Syntax

_8 overloaded forms:_

```pinescript
math.max(number0, number1, ...) → const int
```

```pinescript
math.max(number0, number1, ...) → const float
```

```pinescript
math.max(number0, number1, ...) → simple int
```

```pinescript
math.max(number0, number1, ...) → simple float
```

```pinescript
math.max(number0, number1, ...) → input int
```

```pinescript
math.max(number0, number1, ...) → input float
```

```pinescript
math.max(number0, number1, ...) → series int
```

```pinescript
math.max(number0, number1, ...) → series float
```

## Description

Returns the greatest of multiple values.

## Arguments

- **`number0, number1, ...`** `const int` — A sequence of numbers to use in the calculation.

## Returns

The greatest of multiple given values.

**Return type(s):** `const int`

## Examples

```pinescript
//@version=6
indicator("math.max", overlay=true)
plot(math.max(close, open))
plot(math.max(close, math.max(open, 42)))
```

## See also

- [math.min()](./min.md)
