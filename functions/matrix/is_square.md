---
title: "matrix.is_square"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.is_square
---

# matrix.is_square

**Category:** Function

## Syntax

```pinescript
matrix.is_square(id) → series bool
```

## Description

The function determines if the matrix is [square](https://en.wikipedia.org/wiki/Square_matrix) (it has the same number of rows and columns).

## Arguments

- **`id`** `any matrix type` — Matrix object to test.

## Returns

Returns true if the `id` matrix is square, false otherwise.

**Return type(s):** `series bool`

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.get()](./get.md)
- [matrix.set()](./set.md)
- [matrix.columns()](./columns.md)
- [matrix.rows()](./rows.md)
