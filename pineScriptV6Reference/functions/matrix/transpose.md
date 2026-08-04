---
title: "matrix.transpose"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.transpose
---

# matrix.transpose

**Category:** Function

## Syntax

```pinescript
matrix.transpose(id) → matrix<type>
```

## Description

The function creates a new, [transposed](https://en.wikipedia.org/wiki/Transpose#Transpose_of_a_matrix) version of the `id`. This interchanges the row and column index of each element.

## Arguments

- **`id`** `any matrix type` — A matrix object.

## Returns

A new matrix containing the transposed version of the `id` matrix.

**Return type(s):** `matrix<>`

## Examples

```pinescript
//@version=6
indicator("`matrix.transpose()` Example")

// For efficiency, execute this code only once.
if barstate.islastconfirmedhistory
	// Create a 2x2 matrix.
	var m1 = matrix.new<float>(2, 2, na)
	// Fill the matrix with values.
	matrix.set(m1, 0, 0, 1)
	matrix.set(m1, 0, 1, 2)
	matrix.set(m1, 1, 0, 3)
	matrix.set(m1, 1, 1, 4)

	// Create a transpose of the matrix.
	var m2 = matrix.transpose(m1)

	// Display using a table.
	var t = table.new(position.top_right, 2, 2, color.green)
	table.cell(t, 0, 0, "Original matrix:")
	table.cell(t, 0, 1, str.tostring(m1))
	table.cell(t, 1, 0, "Transposed matrix:")
	table.cell(t, 1, 1, str.tostring(m2))
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.set()](./set.md)
- [matrix.columns()](./columns.md)
- [matrix.rows()](./rows.md)
- [matrix.reshape()](./reshape.md)
- [matrix.reverse()](./reverse.md)
