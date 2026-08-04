---
title: "matrix.eigenvectors"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.eigenvectors
---

# matrix.eigenvectors

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
matrix.eigenvectors(id) → matrix<float>
```

```pinescript
matrix.eigenvectors(id) → matrix<int>
```

## Description

Returns a matrix of [eigenvectors](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors), in which each column is an eigenvector of the `id` matrix.

## Arguments

- **`id`** `matrix<int/float>` — A matrix object.

## Returns

A new matrix containing the eigenvectors of the `id` matrix.

**Return type(s):** `matrix<float>`

## Remarks

The function is calculated using "The Implicit QL Algorithm".

## Examples

```pinescript
//@version=6
indicator("`matrix.eigenvectors()` Example")

// For efficiency, execute this code only once.
if barstate.islastconfirmedhistory
	// Create a 2x2 matrix
	var m1 = matrix.new<int>(2, 2, 1)
	// Fill the matrix with values.
	matrix.set(m1, 0, 0, 2)
	matrix.set(m1, 0, 1, 4)
	matrix.set(m1, 1, 0, 6)
	matrix.set(m1, 1, 1, 8)

	// Get the eigenvectors of the matrix.
	m2 = matrix.eigenvectors(m1)

	// Display matrix elements.
	var t = table.new(position.top_right, 2, 2, color.green)
	table.cell(t, 0, 0, "Matrix Elements:")
	table.cell(t, 0, 1, str.tostring(m1))
	table.cell(t, 1, 0, "Matrix Eigenvectors:")
	table.cell(t, 1, 1, str.tostring(m2))
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.get()](./get.md)
- [matrix.set()](./set.md)
- [matrix.eigenvalues()](./eigenvalues.md)
