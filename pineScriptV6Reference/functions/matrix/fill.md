---
title: "matrix.fill"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.fill
---

# matrix.fill

**Category:** Function

## Syntax

```pinescript
matrix.fill(id, value, from_row, to_row, from_column, to_column) → void
```

## Description

The function fills a rectangular area of the `id` matrix defined by the indices `from_column` to `to_column` (not including it) and `from_row` to `to_row`(not including it) with the `value`.

## Arguments

- **`id`** `any matrix type` — A matrix object.
- **`value`** `series <type of the matrix's elements>` — The value to fill with.
- **`from_row`** `series int` (optional) — Row index from which the fill will begin (inclusive). Optional. The default value is 0.
- **`to_row`** `series int` (optional) — Row index where the fill will end (not inclusive). Optional. The default value is [matrix.rows()](./rows.md).
- **`from_column`** `series int` (optional) — Column index from which the fill will begin (inclusive). Optional. The default value is 0.
- **`to_column`** `series int` (optional) — Column index where the fill will end (non inclusive). Optional. The default value is [matrix.columns()](./columns.md).

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
indicator("`matrix.fill()` Example")

// Create a 4x5 "int" matrix containing values `0`.
m = matrix.new<float>(4, 5, 0)

// Fill the intersection of rows 1 to 2 and columns 2 to 3 of the matrix with `hl2` values.
matrix.fill(m, hl2, 0, 2, 1, 3)

// Display using a label.
if barstate.islastconfirmedhistory
	label.new(bar_index, high, str.tostring(m))
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.get()](./get.md)
- [matrix.set()](./set.md)
- [matrix.columns()](./columns.md)
- [matrix.rows()](./rows.md)
