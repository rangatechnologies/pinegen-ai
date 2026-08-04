---
title: "matrix"
kind: type
source: https://www.tradingview.com/pine-script-reference/v6/#type_matrix
---

# matrix

**Category:** Type

## Description

Keyword used to explicitly declare the "matrix" type of a variable or a parameter. Matrix objects (or IDs) can be created with the [matrix.new<type>()](../functions/matrix/new-type.md) function.

## Remarks

Matrix objects are always of "series" form.

## Examples

```pinescript
//@version=6
indicator("matrix example")

// Create `m1` matrix of `int` type.
matrix<int> m1 = matrix.new<int>(2, 3, 0)

// `matrix<int>` is unnecessary because the `matrix.new<int>()` function returns an `int` type matrix object.
m2 = matrix.new<int>(2, 3, 0)

// Display matrix using a label.
if barstate.islastconfirmedhistory
	label.new(bar_index, high, str.tostring(m2))
```

## See also

- [var](../keywords/var.md)
- [matrix.new<type>()](../functions/matrix/new-type.md)
- [array](./array.md)
