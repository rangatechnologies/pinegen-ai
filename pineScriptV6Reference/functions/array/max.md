---
title: "array.max"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.max
---

# array.max

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
array.max(id, nth) → series float
```

```pinescript
array.max(id, nth) → series int
```

## Description

The function returns the greatest value, or the nth greatest value in a given array.

## Arguments

- **`id`** `array<int/float>` — An array object.
- **`nth`** `series int` — The nth greatest value to return, where zero is the greatest. Optional. The default is zero.

## Returns

The greatest or the nth greatest value in the array.

**Return type(s):** `series float`

## Remarks

Returns [na](../../variables/na.md) if the `id` array is empty.

## Examples

```pinescript
//@version=6
indicator("array.max")
a = array.from(5, -2, 0, 9, 1)
thirdHighest = array.max(a, 2) // 1
plot(thirdHighest)
```

## See also

- [array.new_float()](./new_float.md)
- [array.min()](./min.md)
- [array.sum()](./sum.md)
