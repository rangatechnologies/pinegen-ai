---
title: "matrix.diff"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.diff
---

# matrix.diff

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
matrix.diff(id1, id2) → matrix<int>
```

```pinescript
matrix.diff(id1, id2) → matrix<float>
```

## Description

The function returns a new matrix resulting from the subtraction between matrices `id1` and `id2`, or of matrix `id1` and an `id2` scalar (a numerical value).

## Arguments

- **`id1`** `matrix<int>` — Matrix to subtract from.
- **`id2`** `series int/float/matrix<int>` — Matrix object or a scalar value to be subtracted.

## Returns

A new matrix object containing the difference between `id2` and `id1`.

**Return type(s):** `matrix<int>`

## Detailed Description

Difference between two matrices

```pinescript
//@version=6
indicator("`matrix.diff()` Example 1")

// For efficiency, execute this code only once.
if barstate.islastconfirmedhistory
	// Create a 2x3 matrix containing values `5`.
	var m1 = matrix.new<float>(2, 3, 5)
	// Create a 2x3 matrix containing values `4`.
	var m2 = matrix.new<float>(2, 3, 4)
	// Create a new matrix containing the difference between matrices `m1` and `m2`.
	var m3 = matrix.diff(m1, m2)

	// Display using a table.
	var t = table.new(position.top_right, 1, 2, color.green)
	table.cell(t, 0, 0, "Difference between two matrices:")
	table.cell(t, 0, 1, str.tostring(m3))
```

---

Difference between a matrix and a scalar value

```pinescript
//@version=6
indicator("`matrix.diff()` Example 2")

// For efficiency, execute this code only once.
if barstate.islastconfirmedhistory
	// Create a 2x3 matrix with values `4`.
	var m1 = matrix.new<float>(2, 3, 4)

	// Create a new matrix containing the difference between the `m1` matrix and the "int" value `1`.
	var m2 = matrix.diff(m1, 1)

	// Display using a table.
	var t = table.new(position.top_right, 1, 2, color.green)
	table.cell(t, 0, 0, "Difference between a matrix and a scalar:")
	table.cell(t, 0, 1, str.tostring(m2))
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.get()](./get.md)
- [matrix.set()](./set.md)
- [matrix.columns()](./columns.md)
- [matrix.rows()](./rows.md)
