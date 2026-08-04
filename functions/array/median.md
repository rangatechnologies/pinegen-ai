---
title: "array.median"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.median
---

# array.median

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
array.median(id) → series float
```

```pinescript
array.median(id) → series int
```

## Description

The function returns the median of an array's elements.

## Arguments

- **`id`** `array<int/float>` — An array object.

## Returns

The median of the array's elements.

**Return type(s):** `series float`

## Remarks

Returns [na](../../variables/na.md) if the `id` array is empty.

## Examples

```pinescript
//@version=6
indicator("array.median example")
a = array.new_float(0)
for i = 0 to 9
	array.push(a, close[i])
plot(array.median(a))
```

## See also

- [array.median()](./median.md)
- [array.avg()](./avg.md)
- [array.variance()](./variance.md)
- [array.min()](./min.md)
