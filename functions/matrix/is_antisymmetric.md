---
title: "matrix.is_antisymmetric"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.is_antisymmetric
---

# matrix.is_antisymmetric

**Category:** Function

## Syntax

```pinescript
matrix.is_antisymmetric(id) → series bool
```

## Description

The function determines if a matrix is [antisymmetric](https://en.wikipedia.org/wiki/Skew-symmetric_matrix) (its [transpose](https://en.wikipedia.org/wiki/Transpose) equals its negative).

## Arguments

- **`id`** `matrix<int/float>` — Matrix object to test.

## Returns

Returns true, if the `id` matrix is antisymmetric, false otherwise.

**Return type(s):** `series bool`

## Remarks

Returns false with non-square matrices.

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.get()](./get.md)
- [matrix.set()](./set.md)
- [matrix.is_square()](./is_square.md)
