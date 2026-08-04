---
title: "matrix.rank"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.rank
---

# matrix.rank

**Category:** Function

## Syntax

```pinescript
matrix.rank(id) → series int
```

## Description

The function calculates the [rank](https://en.wikipedia.org/wiki/Rank_(linear_algebra)) of the matrix.

## Arguments

- **`id`** `any matrix type` — A matrix object.

## Returns

The rank of the `id` matrix.

**Return type(s):** `series int`

## Examples

```pinescript
//@version=6
indicator("`matrix.rank()` Example")

// For efficiency, execute this code only once.
if barstate.islastconfirmedhistory
	// Create a 2x2 matrix.
	var m1 = matrix.new<int>(2, 2, na)
	// Fill the matrix with values.
	matrix.set(m1, 0, 0, 1)
	matrix.set(m1, 0, 1, 2)
	matrix.set(m1, 1, 0, 3)
	matrix.set(m1, 1, 1, 4)

	// Get the rank of the matrix.
	r = matrix.rank(m1)

	// Display matrix elements.
	var t = table.new(position.top_right, 2, 2, color.green)
	table.cell(t, 0, 0, "Matrix elements:")
	table.cell(t, 0, 1, str.tostring(m1))
	table.cell(t, 1, 0, "Rank of the matrix:")
	table.cell(t, 1, 1, str.tostring(r))
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.set()](./set.md)
- [str.tostring()](../str/tostring.md)
