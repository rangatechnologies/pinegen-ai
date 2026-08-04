---
title: "matrix.kron"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.kron
---

# matrix.kron

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
matrix.kron(id1, id2) → matrix<float>
```

```pinescript
matrix.kron(id1, id2) → matrix<int>
```

## Description

The function returns the [Kronecker product](https://en.wikipedia.org/wiki/Kronecker_product) for the `id1` and `id2` matrices.

## Arguments

- **`id1`** `matrix<int/float>` — First matrix object.
- **`id2`** `matrix<int/float>` — Second matrix object.

## Returns

A new matrix containing the [Kronecker product](https://en.wikipedia.org/wiki/Kronecker_product) of `id1` and `id2`.

**Return type(s):** `matrix<float>`

## Examples

```pinescript
//@version=6
indicator("`matrix.kron()` Example")

// Display using a table.
if barstate.islastconfirmedhistory
	// Create two matrices with default values `1` and `2`.
	var m1 = matrix.new<float>(2, 2, 1)
	var m2 = matrix.new<float>(2, 2, 2)

	// Calculate the Kronecker product of the matrices.
	var m3 = matrix.kron(m1, m2)

	// Display matrix elements.
	var t = table.new(position.top_right, 5, 2, color.green)
	table.cell(t, 0, 0, "Matrix 1:")
	table.cell(t, 0, 1, str.tostring(m1))
	table.cell(t, 1, 1, "⊗")
	table.cell(t, 2, 0, "Matrix 2:")
	table.cell(t, 2, 1, str.tostring(m2))
	table.cell(t, 3, 1, "=")
	table.cell(t, 4, 0, "Kronecker product:")
	table.cell(t, 4, 1, str.tostring(m3))
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.mult()](./mult.md)
- [str.tostring()](../str/tostring.md)
- [table.new()](../table/new.md)
