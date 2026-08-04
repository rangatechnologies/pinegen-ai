---
title: "matrix.sum"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.sum
---

# matrix.sum

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
matrix.sum(id1, id2) → matrix<int>
```

```pinescript
matrix.sum(id1, id2) → matrix<float>
```

## Description

The function returns a new matrix resulting from the [sum](https://en.wikipedia.org/wiki/Matrix_addition) of two matrices `id1` and `id2`, or of an `id1` matrix and an `id2` scalar (a numerical value).

## Arguments

- **`id1`** `matrix<int>` — First matrix object.
- **`id2`** `series int/float/matrix<int>` — Second matrix object, or scalar value.

## Returns

A new matrix object containing the sum of `id2` and `id1`.

**Return type(s):** `matrix<int>`

## Detailed Description

Sum of two matrices

```pinescript
//@version=6
indicator("`matrix.sum()` Example 1")

// For efficiency, execute this code only once.
if barstate.islastconfirmedhistory
	// Create a 2x3 matrix containing values `5`.
	var m1 = matrix.new<float>(2, 3, 5)
	// Create a 2x3 matrix containing values `4`.
	var m2 = matrix.new<float>(2, 3, 4)
	// Create a new matrix that sums matrices `m1` and `m2`.
	var m3 = matrix.sum(m1, m2)

	// Display using a table.
	var t = table.new(position.top_right, 1, 2, color.green)
	table.cell(t, 0, 0, "Sum of two matrices:")
	table.cell(t, 0, 1, str.tostring(m3))
```

---

Sum of a matrix and scalar

```pinescript
//@version=6
indicator("`matrix.sum()` Example 2")

// For efficiency, execute this code only once.
if barstate.islastconfirmedhistory
	// Create a 2x3 matrix with values `4`.
	var m1 = matrix.new<float>(2, 3, 4)

	// Create a new matrix containing the sum of the `m1` matrix with the "int" value `1`.
	var m2 = matrix.sum(m1, 1)

	// Display using a table.
	var t = table.new(position.top_right, 1, 2, color.green)
	table.cell(t, 0, 0, "Sum of a matrix and a scalar:")
	table.cell(t, 0, 1, str.tostring(m2))
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.get()](./get.md)
- [matrix.set()](./set.md)
- [matrix.columns()](./columns.md)
- [matrix.rows()](./rows.md)
