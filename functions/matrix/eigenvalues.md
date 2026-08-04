---
title: "matrix.eigenvalues"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.eigenvalues
---

# matrix.eigenvalues

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
matrix.eigenvalues(id) → array<float>
```

```pinescript
matrix.eigenvalues(id) → array<int>
```

## Description

The function returns an array containing the [eigenvalues](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) of a square matrix.

## Arguments

- **`id`** `matrix<int/float>` — A matrix object.

## Returns

An array containing the eigenvalues of the `id` matrix.

**Return type(s):** `array<float>`

## Remarks

The function is calculated using "The Implicit QL Algorithm".

## Examples

```pinescript
//@version=6
indicator("`matrix.eigenvalues()` Example")

// For efficiency, execute this code only once.
if barstate.islastconfirmedhistory
	// Create a 2x2 matrix.
	var m1 = matrix.new<int>(2, 2, na)
	// Fill the matrix with values.
	matrix.set(m1, 0, 0, 2)
	matrix.set(m1, 0, 1, 4)
	matrix.set(m1, 1, 0, 6)
	matrix.set(m1, 1, 1, 8)

	// Get the eigenvalues of the matrix.
	tr = matrix.eigenvalues(m1)

	// Display matrix elements.
	var t = table.new(position.top_right, 2, 2, color.green)
	table.cell(t, 0, 0, "Matrix elements:")
	table.cell(t, 0, 1, str.tostring(m1))
	table.cell(t, 1, 0, "Array of Eigenvalues:")
	table.cell(t, 1, 1, str.tostring(tr))
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.set()](./set.md)
- [matrix.eigenvectors()](./eigenvectors.md)
