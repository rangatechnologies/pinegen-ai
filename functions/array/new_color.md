---
title: "array.new_color"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.new_color
---

# array.new_color

**Category:** Function

## Syntax

```pinescript
array.new_color(size, initial_value) → array<color>
```

## Description

The function creates a new array object of color type elements.

## Arguments

- **`size`** `series int` (optional) — Initial size of an array. Optional. The default is 0.
- **`initial_value`** `series color` (optional) — Initial value of all array elements. Optional. The default is 'na'.

## Returns

The ID of an array object which may be used in other array.*() functions.

**Return type(s):** `array<color>`

## Remarks

An array index starts from 0.

## Examples

```pinescript
//@version=6
indicator("array.new_color example")
length = 5
a = array.new_color(length, color.red)
plot(close, color = array.get(a, 0))
```

## See also

- [array.new_float()](./new_float.md)
- [array.get()](./get.md)
- [array.slice()](./slice.md)
- [array.sort()](./sort.md)
