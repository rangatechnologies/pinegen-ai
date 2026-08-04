---
title: "matrix.pinv"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.pinv
---

# matrix.pinv

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
matrix.pinv(id) → matrix<float>
```

```pinescript
matrix.pinv(id) → matrix<int>
```

## Description

The function returns the [pseudoinverse](https://en.wikipedia.org/wiki/Moore%E2%80%93Penrose_inverse) of a matrix.

## Arguments

- **`id`** `matrix<int/float>` — A matrix object.

## Returns

A new matrix containing the pseudoinverse of the `id` matrix.

**Return type(s):** `matrix<float>`

## Remarks

The function is calculated using a [Moore–Penrose](https://en.wikipedia.org/wiki/Moore%E2%80%93Penrose_inverse#Definition) inverse formula based on singular-value decomposition of a matrix. For non-singular square matrices this function returns the result of [matrix.inv()](./inv.md).

## Examples

```pinescript
//@version=6
indicator("`matrix.pinv()` Example")

// For efficiency, execute this code only once.
if barstate.islastconfirmedhistory
	// Create a 2x2 matrix.
	var m1 = matrix.new<int>(2, 2, na)
	// Fill the matrix with values.
	matrix.set(m1, 0, 0, 1)
	matrix.set(m1, 0, 1, 2)
	matrix.set(m1, 1, 0, 3)
	matrix.set(m1, 1, 1, 4)

	// Pseudoinverse of the matrix.
	var m2 = matrix.pinv(m1)

	// Display matrix elements.
	var t = table.new(position.top_right, 2, 2, color.green)
	table.cell(t, 0, 0, "Original Matrix:")
	table.cell(t, 0, 1, str.tostring(m1))
	table.cell(t, 1, 0, "Pseudoinverse matrix:")
	table.cell(t, 1, 1, str.tostring(m2))
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.set()](./set.md)
- [matrix.inv()](./inv.md)
