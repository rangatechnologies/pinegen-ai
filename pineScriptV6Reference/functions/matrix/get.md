---
title: "matrix.get"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.get
---

# matrix.get

**Category:** Function

## Syntax

```pinescript
matrix.get(id, row, column) → <matrix_type>
```

## Description

The function returns the element with the specified index of the matrix.

## Arguments

- **`id`** `any matrix type` — A matrix object.
- **`row`** `series int` — Index of the required row.
- **`column`** `series int` — Index of the required column.

## Returns

The value of the element at the `row` and `column` index of the `id` matrix.

## Remarks

Indexing of the rows and columns starts at zero.

## Examples

```pinescript
//@version=6
indicator("`matrix.get()` Example", "", true)

// Create a 2x3 "float" matrix from the `hl2` values.
m = matrix.new<float>(2, 3, hl2)

// Return the value of the element at index [0, 0] of matrix `m`.
x = matrix.get(m, 0, 0)

plot(x)
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.set()](./set.md)
- [matrix.columns()](./columns.md)
- [matrix.rows()](./rows.md)
