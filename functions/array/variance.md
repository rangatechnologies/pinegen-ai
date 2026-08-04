---
title: "array.variance"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.variance
---

# array.variance

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
array.variance(id, biased) → series float
```

```pinescript
array.variance(id, biased) → series int
```

## Description

The function returns the variance of an array's elements.

## Arguments

- **`id`** `array<int/float>` — An array object.
- **`biased`** `series bool` (optional) — Determines which estimate should be used. Optional. The default is true.

## Returns

The variance of the array's elements.

**Return type(s):** `series float`

## Remarks

If `biased` is true, function will calculate using a biased estimate of the entire population, if false - unbiased estimate of a sample.

Returns [na](../../variables/na.md) if the `id` array is empty.

## Examples

```pinescript
//@version=6
indicator("array.variance example")
a = array.new_float(0)
for i = 0 to 9
	array.push(a, close[i])
plot(array.variance(a))
```

## See also

- [array.new_float()](./new_float.md)
- [array.stdev()](./stdev.md)
- [array.min()](./min.md)
- [array.avg()](./avg.md)
- [array.covariance()](./covariance.md)
