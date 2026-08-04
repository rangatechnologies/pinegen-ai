---
title: "array.standardize"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.standardize
---

# array.standardize

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
array.standardize(id) → array<float>
```

```pinescript
array.standardize(id) → array<int>
```

## Description

The function returns the array of standardized elements.

## Arguments

- **`id`** `array<int/float>` — An array object.

## Returns

The array of standardized elements.

**Return type(s):** `array<float>`

## Examples

```pinescript
//@version=6
indicator("array.standardize example")
a = array.new_float(0)
for i = 0 to 9
	array.push(a, close[i])
b = array.standardize(a)
plot(array.min(b))
plot(array.max(b))
```

## See also

- [array.max()](./max.md)
- [array.min()](./min.md)
- [array.mode()](./mode.md)
- [array.avg()](./avg.md)
- [array.variance()](./variance.md)
- [array.stdev()](./stdev.md)
