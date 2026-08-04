---
title: "matrix.is_triangular"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.is_triangular
---

# matrix.is_triangular

**Category:** Function

## Syntax

```pinescript
matrix.is_triangular(id) → series bool
```

## Description

The function determines if the matrix is [triangular](https://en.wikipedia.org/wiki/Triangular_matrix) (if all elements above or below the [main diagonal](https://en.wikipedia.org/wiki/Main_diagonal) are zero).

## Arguments

- **`id`** `matrix<int/float>` — Matrix object to test.

## Returns

Returns true if the `id` matrix is triangular, false otherwise.

**Return type(s):** `series bool`

## Remarks

Returns false with non-square matrices.

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.set()](./set.md)
- [matrix.is_square()](./is_square.md)
