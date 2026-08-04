---
title: "matrix.col"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.col
---

# matrix.col

**Category:** Function

## Syntax

```pinescript
matrix.col(id, column) → array<type>
```

## Description

The function creates a one-dimensional array from the elements of a matrix column.

## Arguments

- **`id`** `any matrix type` — A matrix object.
- **`column`** `series int` — Index of the required column.

## Returns

An array ID containing the `column` values of the `id` matrix.

**Return type(s):** `array<>`

## Remarks

Indexing of rows starts at 0.

## Examples

```pinescript
//@version=6
indicator("`matrix.col()` Example", "", true)

// Create a 2x3 "float" matrix from `hlc3` values.
m = matrix.new<float>(2, 3, hlc3)

// Return an array with the values of the first column of matrix `m`.
a = matrix.col(m, 0)

// Plot the first value from the array `a`.
plot(array.get(a, 0))
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.get()](./get.md)
- [array.get()](../array/get.md)
- [matrix.col()](./col.md)
- [matrix.columns()](./columns.md)
