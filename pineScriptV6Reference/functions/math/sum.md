---
title: "math.sum"
kind: function
namespace: math
source: https://www.tradingview.com/pine-script-reference/v6/#fun_math.sum
---

# math.sum

**Category:** Function

## Syntax

```pinescript
math.sum(source, length) → series float
```

## Description

The sum function returns the sliding sum of last y values of x.

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).

## Returns

Sum of `source` for `length` bars back.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are ignored; the function calculates on the `length` quantity of non-`na` values.

## See also

- [ta.cum()](../ta/cum.md)
- [for](../../keywords/for.md)
