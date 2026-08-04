---
title: "matrix.is_binary"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.is_binary
---

# matrix.is_binary

**Category:** Function

## Syntax

```pinescript
matrix.is_binary(id) → series bool
```

## Description

The function determines if the matrix is [binary](https://en.wikipedia.org/wiki/Logical_matrix) (when all elements of the matrix are 0 or 1).

## Arguments

- **`id`** `matrix<int/float>` — Matrix object to test.

## Returns

Returns true if the `id` matrix is binary, false otherwise.

**Return type(s):** `series bool`

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.get()](./get.md)
- [matrix.set()](./set.md)
