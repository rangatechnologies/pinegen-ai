---
title: "math.min"
kind: function
namespace: math
source: https://www.tradingview.com/pine-script-reference/v6/#fun_math.min
---

# math.min

**Category:** Function

## Syntax

_8 overloaded forms:_

```pinescript
math.min(number0, number1, ...) → const int
```

```pinescript
math.min(number0, number1, ...) → const float
```

```pinescript
math.min(number0, number1, ...) → simple int
```

```pinescript
math.min(number0, number1, ...) → simple float
```

```pinescript
math.min(number0, number1, ...) → input int
```

```pinescript
math.min(number0, number1, ...) → input float
```

```pinescript
math.min(number0, number1, ...) → series int
```

```pinescript
math.min(number0, number1, ...) → series float
```

## Description

Returns the smallest of multiple values.

## Arguments

- **`number0, number1, ...`** `const int` — A sequence of numbers to use in the calculation.

## Returns

The smallest of multiple given values.

**Return type(s):** `const int`

## Examples

```pinescript
//@version=6
indicator("math.min", overlay=true)
plot(math.min(close, open))
plot(math.min(close, math.min(open, 42)))
```

## See also

- [math.max()](./max.md)
