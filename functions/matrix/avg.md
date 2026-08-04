---
title: "matrix.avg"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.avg
---

# matrix.avg

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
matrix.avg(id) → series float
```

```pinescript
matrix.avg(id) → series int
```

## Description

The function calculates the average of all elements in the matrix.

## Arguments

- **`id`** `matrix<int/float>` — A matrix object.

## Returns

The average value from the `id` matrix.

**Return type(s):** `series float`

## Examples

```pinescript
//@version=6
indicator("`matrix.avg()` Example")

// Create a 2x2 matrix.
var m = matrix.new<int>(2, 2, na)
// Fill the matrix with values.
matrix.set(m, 0, 0, 1)
matrix.set(m, 0, 1, 2)
matrix.set(m, 1, 0, 3)
matrix.set(m, 1, 1, 4)

// Get the average value of the matrix.
var x = matrix.avg(m)

plot(x, 'Matrix average value')
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.get()](./get.md)
- [matrix.set()](./set.md)
- [matrix.columns()](./columns.md)
- [matrix.rows()](./rows.md)
