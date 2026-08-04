---
title: "array.new_float"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.new_float
---

# array.new_float

**Category:** Function

## Syntax

```pinescript
array.new_float(size, initial_value) → array<float>
```

## Description

The function creates a new array object of float type elements.

## Arguments

- **`size`** `series int` (optional) — Initial size of an array. Optional. The default is 0.
- **`initial_value`** `series int/float` (optional) — Initial value of all array elements. Optional. The default is 'na'.

## Returns

The ID of an array object which may be used in other array.*() functions.

**Return type(s):** `array<float>`

## Remarks

An array index starts from 0.

## Examples

```pinescript
//@version=6
indicator("array.new_float example")
length = 5
a = array.new_float(length, close)
plot(array.sum(a) / length)
```

## See also

- [array.new_color()](./new_color.md)
- [array.new_bool()](./new_bool.md)
- [array.get()](./get.md)
- [array.slice()](./slice.md)
- [array.sort()](./sort.md)
