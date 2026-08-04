---
title: "matrix.columns"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.columns
---

# matrix.columns

**Category:** Function

## Syntax

```pinescript
matrix.columns(id) → series int
```

## Description

The function returns the number of columns in the matrix.

## Arguments

- **`id`** `any matrix type` — A matrix object.

## Returns

The number of columns in the matrix `id`.

**Return type(s):** `series int`

## Examples

```pinescript
//@version=6
indicator("`matrix.columns()` Example")

// Create a 2x6 matrix with values `0`.
var m = matrix.new<int>(2, 6, 0)

// Get the quantity of columns in matrix `m`.
var x = matrix.columns(m)

// Display using a label.
if barstate.islastconfirmedhistory
	label.new(bar_index, high, "Columns: " + str.tostring(x) + "\n" + str.tostring(m))
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.get()](./get.md)
- [matrix.set()](./set.md)
- [matrix.col()](./col.md)
- [matrix.row()](./row.md)
- [matrix.rows()](./rows.md)
