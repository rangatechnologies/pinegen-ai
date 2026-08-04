---
title: "matrix.is_identity"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.is_identity
---

# matrix.is_identity

**Category:** Function

## Syntax

```pinescript
matrix.is_identity(id) → series bool
```

## Description

The function determines if a matrix is an [identity matrix](https://en.wikipedia.org/wiki/Identity_matrix) (elements with ones on the [main diagonal](https://en.wikipedia.org/wiki/Main_diagonal) and zeros elsewhere).

## Arguments

- **`id`** `matrix<int/float>` — Matrix object to test.

## Returns

Returns true if `id` is an identity matrix, false otherwise.

**Return type(s):** `series bool`

## Remarks

Returns false with non-square matrices.

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.is_square()](./is_square.md)
- [matrix.is_diagonal()](./is_diagonal.md)
