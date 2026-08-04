---
title: "matrix.sort"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.sort
---

# matrix.sort

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
matrix.sort(id, column, order) → void
```

```pinescript
matrix.sort(id, column, order, sort_field) → void
```

## Description

The function rearranges the rows in the `id` matrix following the sorted order of the values in the `column`.

## Arguments

- **`id`** `matrix<int/float/string>` — A matrix object to be sorted.
- **`column`** `series int` (optional) — Index of the column whose sorted values determine the new order of rows. Optional. The default value is 0.
- **`order`** `series sort_order` (optional) — The sort order. Possible values: [order.ascending](../../constants/order/ascending.md) (default), [order.descending](../../constants/order/descending.md).

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
indicator("`matrix.sort()` Example")

// For efficiency, execute this code only once.
if barstate.islastconfirmedhistory
	// Create a 2x2 matrix.
	var m1 = matrix.new<float>(2, 2, na)
	// Fill the matrix with values.
	matrix.set(m1, 0, 0, 3)
	matrix.set(m1, 0, 1, 4)
	matrix.set(m1, 1, 0, 1)
	matrix.set(m1, 1, 1, 2)

	// Copy the matrix to a new one.
	var m2 = matrix.copy(m1)
	// Sort the rows of `m2` using the default arguments (first column and ascending order).
	matrix.sort(m2)

	// Display using a table.
	if barstate.islastconfirmedhistory
		var t = table.new(position.top_right, 2, 2, color.green)
		table.cell(t, 0, 0, "Original matrix:")
		table.cell(t, 0, 1, str.tostring(m1))
		table.cell(t, 1, 0, "Sorted matrix:")
		table.cell(t, 1, 1, str.tostring(m2))
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.max()](./max.md)
- [matrix.min()](./min.md)
- [matrix.avg()](./avg.md)
