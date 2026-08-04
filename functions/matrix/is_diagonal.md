---
title: "matrix.is_diagonal"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.is_diagonal
---

# matrix.is_diagonal

**Category:** Function

## Syntax

```pinescript
matrix.is_diagonal(id) → series bool
```

## Description

The function determines if the matrix is [diagonal](https://en.wikipedia.org/wiki/Diagonal_matrix) (all elements outside the main diagonal are zero).

## Arguments

- **`id`** `matrix<int/float>` — Matrix object to test.

## Returns

Returns true if the `id` matrix is diagonal, false otherwise.

**Return type(s):** `series bool`

## Remarks

Returns false with non-square matrices.

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.set()](./set.md)
- [matrix.is_square()](./is_square.md)
- [matrix.is_identity()](./is_identity.md)
- [matrix.is_antidiagonal()](./is_antidiagonal.md)
