---
title: "array.covariance"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.covariance
---

# array.covariance

**Category:** Function

## Syntax

```pinescript
array.covariance(id1, id2, biased) → series float
```

## Description

The function returns the covariance of two arrays.

## Arguments

- **`id1`** `array<int/float>` — An array object.
- **`id2`** `array<int/float>` — An array object.
- **`biased`** `series bool` (optional) — Determines which estimate should be used. Optional. The default is true.

## Returns

The covariance of two arrays.

**Return type(s):** `series float`

## Remarks

If `biased` is [true](../../constants/true.md), function will calculate using a biased estimate of the entire population, if [false](../../constants/false.md) - unbiased estimate of a sample. Returns [na](../../variables/na.md) if both arrays are empty.

## Examples

```pinescript
//@version=6
indicator("array.covariance example")
a = array.new_float(0)
b = array.new_float(0)
for i = 0 to 9
	array.push(a, close[i])
	array.push(b, open[i])
plot(array.covariance(a, b))
```

## See also

- [array.new_float()](./new_float.md)
- [array.max()](./max.md)
- [array.stdev()](./stdev.md)
- [array.avg()](./avg.md)
- [array.variance()](./variance.md)
