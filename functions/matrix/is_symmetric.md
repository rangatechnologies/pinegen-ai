---
title: "matrix.is_symmetric"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.is_symmetric
---

# matrix.is_symmetric

**Category:** Function

## Syntax

```pinescript
matrix.is_symmetric(id) → series bool
```

## Description

The function determines if a [square matrix](https://en.wikipedia.org/wiki/Square_matrix) is [symmetric](https://en.wikipedia.org/wiki/Symmetric_matrix) (elements are symmetric with respect to the [main diagonal](https://en.wikipedia.org/wiki/Main_diagonal)).

## Arguments

- **`id`** `matrix<int/float>` — Matrix object to test.

## Returns

Returns true if the `id` matrix is symmetric, false otherwise.

**Return type(s):** `series bool`

## Remarks

Returns false with non-square matrices.

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.get()](./get.md)
- [matrix.set()](./set.md)
- [matrix.is_square()](./is_square.md)
