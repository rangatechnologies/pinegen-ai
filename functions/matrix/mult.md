---
title: "matrix.mult"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.mult
---

# matrix.mult

**Category:** Function

## Syntax

_4 overloaded forms:_

```pinescript
matrix.mult(id1, id2) → matrix<int>
```

```pinescript
matrix.mult(id1, id2) → matrix<float>
```

```pinescript
matrix.mult(id1, id2) → array<int>
```

```pinescript
matrix.mult(id1, id2) → array<float>
```

## Description

The function returns a new matrix resulting from the [product](https://en.wikipedia.org/wiki/Matrix_multiplication) between the matrices `id1` and `id2`, or between an `id1` matrix and an `id2` scalar (a numerical value), or between an `id1` matrix and an `id2` vector (an array of values).

## Arguments

- **`id1`** `matrix<int>` — First matrix object.
- **`id2`** `series int/float/matrix<int>` — Second matrix object, value or array.

## Returns

A new matrix object containing the product of `id2` and `id1`.

**Return type(s):** `matrix<int>`

## Detailed Description

Product of two matrices

```pinescript
//@version=6
indicator("`matrix.mult()` Example 1")

// For efficiency, execute this code only once.
if barstate.islastconfirmedhistory
	// Create a 6x2 matrix containing values `5`.
	var m1 = matrix.new<float>(6, 2, 5)
	// Create a 2x3 matrix containing values `4`.
	// Note that it must have the same quantity of rows as there are columns in the first matrix.
	var m2 = matrix.new<float>(2, 3, 4)
	// Create a new matrix from the multiplication of the two matrices.
	var m3 = matrix.mult(m1, m2)

	// Display using a table.
	var t = table.new(position.top_right, 1, 2, color.green)
	table.cell(t, 0, 0, "Product of two matrices:")
	table.cell(t, 0, 1, str.tostring(m3))
```

---

Product of a matrix and a scalar

```pinescript
//@version=6
indicator("`matrix.mult()` Example 2")

// For efficiency, execute this code only once.
if barstate.islastconfirmedhistory
	// Create a 2x3 matrix containing values `4`.
	var m1 = matrix.new<float>(2, 3, 4)

	// Create a new matrix from the product of the two matrices.
	scalar = 5
	var m2 = matrix.mult(m1, scalar)

	// Display using a table.
	var t = table.new(position.top_right, 5, 2, color.green)
	table.cell(t, 0, 0, "Matrix 1:")
	table.cell(t, 0, 1, str.tostring(m1))
	table.cell(t, 1, 1, "x")
	table.cell(t, 2, 0, "Scalar:")
	table.cell(t, 2, 1, str.tostring(scalar))
	table.cell(t, 3, 1, "=")
	table.cell(t, 4, 0, "Matrix 2:")
	table.cell(t, 4, 1, str.tostring(m2))
```

---

Product of a matrix and an array vector

```pinescript
//@version=6
indicator("`matrix.mult()` Example 3")

// For efficiency, execute this code only once.
if barstate.islastconfirmedhistory
	// Create a 2x3 matrix containing values `4`.
	var m1 = matrix.new<int>(2, 3, 4)

	// Create an array of three elements.
	var array<int> a = array.from(1, 1, 1)

	// Create a new matrix containing the product of the `m1` matrix and the `a` array.
	var m3 = matrix.mult(m1, a)

	// Display using a table.
	var t = table.new(position.top_right, 5, 2, color.green)
	table.cell(t, 0, 0, "Matrix 1:")
	table.cell(t, 0, 1, str.tostring(m1))
	table.cell(t, 1, 1, "x")
	table.cell(t, 2, 0, "Value:")
	table.cell(t, 2, 1, str.tostring(a, " "))
	table.cell(t, 3, 1, "=")
	table.cell(t, 4, 0, "Matrix 3:")
	table.cell(t, 4, 1, str.tostring(m3))
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.sum()](./sum.md)
- [matrix.diff()](./diff.md)
