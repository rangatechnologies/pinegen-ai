---
title: "matrix.rows"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.rows
---

# matrix.rows

**Category:** Function

## Syntax

```pinescript
matrix.rows(id) → series int
```

## Description

The function returns the number of rows in the matrix.

## Arguments

- **`id`** `any matrix type` — A matrix object.

## Returns

The number of rows in the matrix `id`.

**Return type(s):** `series int`

## Examples

```pinescript
//@version=6
indicator("`matrix.rows()` Example")

// Create a 2x6 matrix with values `0`.
var m = matrix.new<int>(2, 6, 0)

// Get the quantity of rows in the matrix.
var x = matrix.rows(m)

// Display using a label.
if barstate.islastconfirmedhistory
	label.new(bar_index, high, "Rows: " + str.tostring(x) + "\n" + str.tostring(m))
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.get()](./get.md)
- [matrix.set()](./set.md)
- [matrix.columns()](./columns.md)
- [matrix.row()](./row.md)
