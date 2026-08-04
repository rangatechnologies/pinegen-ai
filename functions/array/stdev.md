---
title: "array.stdev"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.stdev
---

# array.stdev

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
array.stdev(id, biased) → series float
```

```pinescript
array.stdev(id, biased) → series int
```

## Description

The function returns the standard deviation of an array's elements.

## Arguments

- **`id`** `array<int/float>` — An array object.
- **`biased`** `series bool` (optional) — Determines which estimate should be used. Optional. The default is true.

## Returns

The standard deviation of the array's elements.

**Return type(s):** `series float`

## Remarks

If `biased` is true, the function calculates using a biased estimate of the entire population. If `biased` is false, it uses an unbiased estimate of a sample.

Returns [na](../../variables/na.md) if the `id` array is empty.

## Examples

```pinescript
//@version=6
indicator("array.stdev example")
a = array.new_float(0)
for i = 0 to 9
	array.push(a, close[i])
plot(array.stdev(a))
```

## See also

- [array.new_float()](./new_float.md)
- [array.max()](./max.md)
- [array.min()](./min.md)
- [array.avg()](./avg.md)
