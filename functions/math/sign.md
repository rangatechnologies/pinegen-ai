---
title: "math.sign"
kind: function
namespace: math
source: https://www.tradingview.com/pine-script-reference/v6/#fun_math.sign
---

# math.sign

**Category:** Function

## Syntax

_4 overloaded forms:_

```pinescript
math.sign(number) → simple float
```

```pinescript
math.sign(number) → input float
```

```pinescript
math.sign(number) → const float
```

```pinescript
math.sign(number) → series float
```

## Description

Sign (signum) of `number` is zero if `number` is zero, 1.0 if `number` is greater than zero, -1.0 if `number` is less than zero.

## Arguments

- **`number`** `simple int/float` — The number to use in the calculation.

## Returns

The sign of the argument.

**Return type(s):** `simple float`
