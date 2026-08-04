---
title: "matrix.concat"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.concat
---

# matrix.concat

**Category:** Function

## Syntax

```pinescript
matrix.concat(id1, id2) → matrix<type>
```

## Description

The function appends the `m2` matrix to the `m1` matrix.

## Arguments

- **`id1`** `any matrix type` — Matrix object to concatenate into.
- **`id2`** `any matrix type` — Matrix object whose elements will be appended to `id1`.

## Returns

Returns the `id1` matrix concatenated with the `id2` matrix.

**Return type(s):** `matrix<>`

## Remarks

The number of columns in both matrices must be identical.

## Examples

```pinescript
//@version=6
indicator("`matrix.concat()` Example")

// Create a 2x4 "int" matrix containing values `0`.
m1 = matrix.new<int>(2, 4, 0)
// Create a 2x4 "int" matrix containing values `1`.
m2 = matrix.new<int>(2, 4, 1)

// Append matrix `m2` to `m1`.
matrix.concat(m1, m2)

// Display matrix elements.
if barstate.islastconfirmedhistory
	var t = table.new(position.top_right, 2, 2, color.green)
	table.cell(t, 0, 0, "Matrix Elements:")
	table.cell(t, 0, 1, str.tostring(m1))
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.get()](./get.md)
- [matrix.set()](./set.md)
- [matrix.columns()](./columns.md)
- [matrix.rows()](./rows.md)
