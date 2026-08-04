---
title: "array.min"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.min
---

# array.min

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
array.min(id, nth) → series float
```

```pinescript
array.min(id, nth) → series int
```

## Description

The function returns the smallest value, or the nth smallest value in a given array.

## Arguments

- **`id`** `array<int/float>` — An array object.
- **`nth`** `series int` — The nth smallest value to return, where zero is the smallest. Optional. The default is zero.

## Returns

The smallest or the nth smallest value in the array.

**Return type(s):** `series float`

## Remarks

Returns [na](../../variables/na.md) if the `id` array is empty.

## Examples

```pinescript
//@version=6
indicator("array.min")
a = array.from(5, -2, 0, 9, 1)
secondLowest = array.min(a, 1) // 0
plot(secondLowest)
```

## See also

- [array.new_float()](./new_float.md)
- [array.max()](./max.md)
- [array.sum()](./sum.md)
