---
title: "array.range"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.range
---

# array.range

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
array.range(id) → series float
```

```pinescript
array.range(id) → series int
```

## Description

The function returns the difference between the min and max values from a given array.

## Arguments

- **`id`** `array<int/float>` — An array object.

## Returns

The difference between the min and max values in the array.

**Return type(s):** `series float`

## Remarks

Returns [na](../../variables/na.md) if the `id` array is empty.

## Examples

```pinescript
//@version=6
indicator("array.range example")
a = array.new_float(0)
for i = 0 to 9
	array.push(a, close[i])
plot(array.range(a))
```

## See also

- [array.new_float()](./new_float.md)
- [array.min()](./min.md)
- [array.max()](./max.md)
- [array.sum()](./sum.md)
