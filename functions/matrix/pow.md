---
title: "matrix.pow"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.pow
---

# matrix.pow

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
matrix.pow(id, power) → matrix<float>
```

```pinescript
matrix.pow(id, power) → matrix<int>
```

## Description

The function calculates the product of the matrix by itself `power` times.

## Arguments

- **`id`** `matrix<int/float>` — A matrix object.
- **`power`** `series int` — The number of times the matrix will be multiplied by itself.

## Returns

The product of the `id` matrix by itself `power` times.

**Return type(s):** `matrix<float>`

## Examples

```pinescript
//@version=6
indicator("`matrix.pow()` Example")

// Display using a table.
if barstate.islastconfirmedhistory
	// Create a 2x2 matrix.
	var m1 = matrix.new<int>(2, 2, 2)
	// Calculate the power of three of the matrix.
	var m2 = matrix.pow(m1, 3)

	// Display matrix elements.
	var t = table.new(position.top_right, 2, 2, color.green)
	table.cell(t, 0, 0, "Original Matrix:")
	table.cell(t, 0, 1, str.tostring(m1))
	table.cell(t, 1, 0, "Matrix³:")
	table.cell(t, 1, 1, str.tostring(m2))
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.set()](./set.md)
- [matrix.mult()](./mult.md)
