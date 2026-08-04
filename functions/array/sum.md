---
title: "array.sum"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.sum
---

# array.sum

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
array.sum(id) → series float
```

```pinescript
array.sum(id) → series int
```

## Description

The function returns the sum of an array's elements.

## Arguments

- **`id`** `array<int/float>` — An array object.

## Returns

The sum of the array's elements.

**Return type(s):** `series float`

## Remarks

Returns [na](../../variables/na.md) if the `id` array is empty.

## Examples

```pinescript
//@version=6
indicator("array.sum example")
a = array.new_float(0)
for i = 0 to 9
	array.push(a, close[i])
plot(array.sum(a))
```

## See also

- [array.new_float()](./new_float.md)
- [array.max()](./max.md)
- [array.min()](./min.md)
