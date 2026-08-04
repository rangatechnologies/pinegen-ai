---
title: "matrix.add_col"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.add_col
---

# matrix.add_col

**Category:** Function

## Syntax

```pinescript
matrix.add_col(id, column, array_id) → void
```

## Description

Inserts a new column at the `column` index of the `id` matrix.

## Arguments

- **`id`** `any matrix type` — The matrix object's ID (reference).
- **`column`** `series int` (optional) — Optional. The index of the new column. Must be a value from 0 to `matrix.columns(id)`. All existing columns with indices that are greater than or equal to this value increase their index by one. The default is `matrix.columns(id)`.
- **`array_id`** `any array type` — Optional. The ID of an array to use as the new column. If the matrix is empty, the array can be of any size. Otherwise, its size must equal `matrix.rows(id)`. By default, the function inserts a column of [na](../../variables/na.md) values.

**Return type(s):** `void`

## Remarks

Rather than add columns to an empty matrix, it is far more efficient to declare a matrix with explicit dimensions and fill it with values. Adding a column is also much slower than adding a row with the [matrix.add_row()](./add_row.md) function.

## Detailed Description

Adding a column to the matrix

```pinescript
//@version=6
indicator("`matrix.add_col()` Example 1")

// Create a 2x3 "int" matrix containing values `0`.
m = matrix.new<int>(2, 3, 0)

// Add a column with `na` values to the matrix.
matrix.add_col(m)

// Display matrix elements.
if barstate.islastconfirmedhistory
	var t = table.new(position.top_right, 2, 2, color.green)
	table.cell(t, 0, 0, "Matrix elements:")
	table.cell(t, 0, 1, str.tostring(m))
```

---

Adding an array as a column to the matrix

```pinescript
//@version=6
indicator("`matrix.add_col()` Example 2")

if barstate.islastconfirmedhistory
	// Create an empty matrix object.
	var m = matrix.new<int>()

	// Create an array with values `1` and `3`.
	var a = array.from(1, 3)

	// Add the `a` array as the first column of the empty matrix.
	matrix.add_col(m, 0, a)

	// Display matrix elements.
	var t = table.new(position.top_right, 2, 2, color.green)
	table.cell(t, 0, 0, "Matrix elements:")
	table.cell(t, 0, 1, str.tostring(m))
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.get()](./get.md)
- [matrix.set()](./set.md)
- [matrix.columns()](./columns.md)
- [matrix.rows()](./rows.md)
- [matrix.add_row()](./add_row.md)
