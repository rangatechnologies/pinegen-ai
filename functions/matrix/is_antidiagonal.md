---
title: "matrix.is_antidiagonal"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.is_antidiagonal
---

# matrix.is_antidiagonal

**Category:** Function

## Syntax

```pinescript
matrix.is_antidiagonal(id) → series bool
```

## Description

The function determines if the matrix is [anti-diagonal](https://en.wikipedia.org/wiki/Anti-diagonal_matrix) (all elements outside the secondary diagonal are zero).

## Arguments

- **`id`** `matrix<int/float>` — Matrix object to test.

## Returns

Returns true if the `id` matrix is ​​anti-diagonal, false otherwise.

**Return type(s):** `series bool`

## Remarks

Returns false with non-square matrices.

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.set()](./set.md)
- [matrix.is_square()](./is_square.md)
- [matrix.is_identity()](./is_identity.md)
- [matrix.is_diagonal()](./is_diagonal.md)
