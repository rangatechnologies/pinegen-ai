---
title: "matrix.row"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.row
---

# matrix.row

**Category:** Function

## Syntax

```pinescript
matrix.row(id, row) → array<type>
```

## Description

The function creates a one-dimensional array from the elements of a matrix row.

## Arguments

- **`id`** `any matrix type` — A matrix object.
- **`row`** `series int` — Index of the required row.

## Returns

An array ID containing the `row` values of the `id` matrix.

**Return type(s):** `array<>`

## Remarks

Indexing of rows starts at 0.

## Examples

```pinescript
//@version=6
indicator("`matrix.row()` Example", "", true)

// Create a 2x3 "float" matrix from `hlc3` values.
m = matrix.new<float>(2, 3, hlc3)

// Return an array with the values of the first row of the matrix.
a = matrix.row(m, 0)

// Plot the first value from the array `a`.
plot(array.get(a, 0))
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.get()](./get.md)
- [array.get()](../array/get.md)
- [matrix.col()](./col.md)
- [matrix.rows()](./rows.md)
