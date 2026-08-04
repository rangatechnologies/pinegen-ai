---
title: "matrix.mode"
kind: function
namespace: matrix
source: https://www.tradingview.com/pine-script-reference/v6/#fun_matrix.mode
---

# matrix.mode

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
matrix.mode(id) → series float
```

```pinescript
matrix.mode(id) → series int
```

## Description

The function calculates the [mode](https://en.wikipedia.org/wiki/Mode_(statistics)) of the matrix, which is the most frequently occurring value from the matrix elements. When there are multiple values occurring equally frequently, the function returns the smallest of those values.

## Arguments

- **`id`** `matrix<int/float>` — A matrix object.

## Returns

The most frequently occurring value from the `id` matrix. If none exists, returns the smallest value instead.

**Return type(s):** `series float`

## Remarks

Note that [na](../../variables/na.md) elements of the matrix are not considered when calculating the mode.

## Examples

```pinescript
//@version=6
indicator("`matrix.mode()` Example")

// Create a 2x2 matrix.
var m = matrix.new<int>(2, 2, na)
// Fill the matrix with values.
matrix.set(m, 0, 0, 0)
matrix.set(m, 0, 1, 0)
matrix.set(m, 1, 0, 1)
matrix.set(m, 1, 1, 1)

// Get the mode of the matrix.
var x = matrix.mode(m)

plot(x, 'Mode of the matrix')
```

## See also

- [matrix.new<type>()](./new-type.md)
- [matrix.set()](./set.md)
- [matrix.median()](./median.md)
- [matrix.sort()](./sort.md)
- [matrix.avg()](./avg.md)
