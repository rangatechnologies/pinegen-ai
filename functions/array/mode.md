---
title: "array.mode"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.mode
---

# array.mode

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
array.mode(id) → series float
```

```pinescript
array.mode(id) → series int
```

## Description

The function returns the mode of an array's elements. If there are several values with the same frequency, it returns the smallest value.

## Arguments

- **`id`** `array<int/float>` — An array object.

## Returns

The most frequently occurring value from the `id` array. If none exists, returns the smallest value instead.

**Return type(s):** `series float`

## Remarks

Returns [na](../../variables/na.md) if the `id` array is empty.

## Examples

```pinescript
//@version=6
indicator("array.mode example")
a = array.new_float(0)
for i = 0 to 9
	array.push(a, close[i])
plot(array.mode(a))
```

## See also

- [array.new_float()](./new_float.md)
- [ta.mode()](../ta/mode.md)
- [matrix.mode()](../matrix/mode.md)
- [array.avg()](./avg.md)
- [array.variance()](./variance.md)
- [array.min()](./min.md)
