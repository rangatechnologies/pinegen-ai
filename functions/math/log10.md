---
title: "math.log10"
kind: function
namespace: math
source: https://www.tradingview.com/pine-script-reference/v6/#fun_math.log10
---

# math.log10

**Category:** Function

## Syntax

_4 overloaded forms:_

```pinescript
math.log10(number) → simple float
```

```pinescript
math.log10(number) → input float
```

```pinescript
math.log10(number) → const float
```

```pinescript
math.log10(number) → series float
```

## Description

The common (or base 10) logarithm of `number` is the power to which 10 must be raised to obtain the `number`. 10^y = `number`.

## Arguments

- **`number`** `simple int/float` — The number to use in the calculation.

## Returns

The base 10 logarithm of `number`.

**Return type(s):** `simple float`

## See also

- [math.log()](./log.md)
