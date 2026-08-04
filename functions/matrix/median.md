---
title: "matrix.median"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.median
---

# matrix.median

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
matrix.median(id) → series float
```

```pinescript
matrix.median(id) → series int
```

## Description

The function calculates the [median](https://en.wikipedia.org/wiki/Median) ("the middle" value) of matrix elements.

## Arguments

- **`id`** `matrix<int/float>` — A matrix object.

**Return type(s):** `series float`

## Remarks

Note that [na](../../variables/na.md) elements of the matrix are not considered when calculating the median.

## Examples

```pinescript
//@version=6
indicator("`matrix.median()` Example")

// Create a 2x2 matrix.
m = matrix.new<int>(2, 2, na)
// Fill the matrix with values.
matrix.set(m, 0, 0, 1)
matrix.set(m, 0, 1, 2)
matrix.set(m, 1, 0, 3)
matrix.set(m, 1, 1, 4)

// Get the median of the matrix.
x = matrix.median(m)

plot(x, 'Median of the matrix')
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.mode()](./mode.md)
- [matrix.sort()](./sort.md)
- [matrix.avg()](./avg.md)
