---
title: "matrix.min"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.min
---

# matrix.min

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
matrix.min(id) → series float
```

```pinescript
matrix.min(id) → series int
```

## Description

The function returns the smallest value from the matrix elements.

## Arguments

- **`id`** `matrix<int/float>` — A matrix object.

## Returns

The smallest value from the `id` matrix.

**Return type(s):** `series float`

## Examples

```pinescript
//@version=6
indicator("`matrix.min()` Example")

// Create a 2x2 matrix.
var m = matrix.new<int>(2, 2, na)
// Fill the matrix with values.
matrix.set(m, 0, 0, 1)
matrix.set(m, 0, 1, 2)
matrix.set(m, 1, 0, 3)
matrix.set(m, 1, 1, 4)

// Get the minimum value from the matrix.
var x = matrix.min(m)

plot(x, 'Matrix minimum value')
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.max()](./max.md)
- [matrix.avg()](./avg.md)
- [matrix.sort()](./sort.md)
