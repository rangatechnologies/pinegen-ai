---
title: "matrix.submatrix"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.submatrix
---

# matrix.submatrix

**Category:** Function

## Syntax

```pinescript
matrix.submatrix(id, from_row, to_row, from_column, to_column) → matrix<type>
```

## Description

The function extracts a submatrix of the `id` matrix within the specified indices.

## Arguments

- **`id`** `any matrix type` — A matrix object.
- **`from_row`** `series int` (optional) — Index of the row from which the extraction will begin (inclusive). Optional. The default value is 0.
- **`to_row`** `series int` (optional) — Index of the row where the extraction will end (non inclusive). Optional. The default value is [matrix.rows()](./rows.md).
- **`from_column`** `series int` (optional) — Index of the column from which the extraction will begin (inclusive). Optional. The default value is 0.
- **`to_column`** `series int` (optional) — Index of the column where the extraction will end (non inclusive). Optional. The default value is [matrix.columns()](./columns.md).

## Returns

A new matrix object containing the submatrix of the `id` matrix defined by the `from_row`, `to_row`, `from_column` and `to_column` indices.

**Return type(s):** `matrix<>`

## Remarks

Indexing of the rows and columns starts at zero.

## Examples

```pinescript
//@version=6
indicator("`matrix.submatrix()` Example")

// For efficiency, execute this code only once.
if barstate.islastconfirmedhistory
	// Create a 2x3 matrix matrix with values `0`.
	var m1 = matrix.new<int>(2, 3, 0)
	// Fill the matrix with values.
	matrix.set(m1, 0, 0, 1)
	matrix.set(m1, 0, 1, 2)
	matrix.set(m1, 0, 2, 3)
	matrix.set(m1, 1, 0, 4)
	matrix.set(m1, 1, 1, 5)
	matrix.set(m1, 1, 2, 6)

	// Create a 2x2 submatrix of the `m1` matrix.
	var m2 = matrix.submatrix(m1, 0, 2, 1, 3)

	// Display using a table.
	var t = table.new(position.top_right, 2, 2, color.green)
	table.cell(t, 0, 0, "Original Matrix:")
	table.cell(t, 0, 1, str.tostring(m1))
	table.cell(t, 1, 0, "Submatrix:")
	table.cell(t, 1, 1, str.tostring(m2))
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.set()](./set.md)
- [matrix.row()](./row.md)
- [matrix.col()](./col.md)
- [matrix.reshape()](./reshape.md)
