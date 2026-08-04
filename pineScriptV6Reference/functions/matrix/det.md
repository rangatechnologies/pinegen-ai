---
title: "matrix.det"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.det
---

# matrix.det

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
matrix.det(id) → series float
```

```pinescript
matrix.det(id) → series int
```

## Description

The function returns the [determinant](https://en.wikipedia.org/wiki/Determinant) of a square matrix.

## Arguments

- **`id`** `matrix<int/float>` — A matrix object.

## Returns

The determinant value of the `id` matrix.

**Return type(s):** `series float`

## Remarks

Function calculation based on the [LU decomposition](https://en.wikipedia.org/wiki/LU_decomposition) algorithm.

## Examples

```pinescript
//@version=6
indicator("`matrix.det` Example")

// Create a 2x2 matrix.
var m = matrix.new<float>(2, 2, na)
// Fill the matrix with values.
matrix.set(m, 0, 0,  3)
matrix.set(m, 0, 1,  7)
matrix.set(m, 1, 0,  1)
matrix.set(m, 1, 1, -4)

// Get the determinant of the matrix.
var x = matrix.det(m)

plot(x, 'Matrix determinant')
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.set()](./set.md)
- [matrix.is_square()](./is_square.md)
