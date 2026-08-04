---
title: "matrix.reshape"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.reshape
---

# matrix.reshape

**Category:** Function

## Syntax

```pinescript
matrix.reshape(id, rows, columns) → void
```

## Description

The function rebuilds the `id` matrix to `rows` x `cols` dimensions.

## Arguments

- **`id`** `any matrix type` — A matrix object.
- **`rows`** `series int` — The number of rows of the reshaped matrix.
- **`columns`** `series int` — The number of columns of the reshaped matrix.

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
indicator("`matrix.reshape()` Example")

// For efficiency, execute this code only once.
if barstate.islastconfirmedhistory
	// Create a 2x3 matrix.
	var m1 = matrix.new<float>(2, 3)
	// Fill the matrix with values.
	matrix.set(m1, 0, 0, 1)
	matrix.set(m1, 0, 1, 2)
	matrix.set(m1, 0, 2, 3)
	matrix.set(m1, 1, 0, 4)
	matrix.set(m1, 1, 1, 5)
	matrix.set(m1, 1, 2, 6)

	// Copy the matrix to a new one.
	var m2 = matrix.copy(m1)

	// Reshape the copy to a 3x2.
	matrix.reshape(m2, 3, 2)

	// Display using a table.
	var t = table.new(position.top_right, 2, 2, color.green)
	table.cell(t, 0, 0, "Original matrix:")
	table.cell(t, 0, 1, str.tostring(m1))
	table.cell(t, 1, 0, "Reshaped matrix:")
	table.cell(t, 1, 1, str.tostring(m2))
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.get()](./get.md)
- [matrix.set()](./set.md)
- [matrix.add_row()](./add_row.md)
- [matrix.add_col()](./add_col.md)
