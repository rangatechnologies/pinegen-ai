---
title: "array.new_bool"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.new_bool
---

# array.new_bool

**Category:** Function

## Syntax

```pinescript
array.new_bool(size, initial_value) → array<bool>
```

## Description

The function creates a new array object of bool type elements.

## Arguments

- **`size`** `series int` (optional) — Initial size of an array. Optional. The default is 0.
- **`initial_value`** `series bool` (optional) — Initial value of all array elements. Optional. The default is 'false'.

## Returns

The ID of an array object which may be used in other array.*() functions.

**Return type(s):** `array<bool>`

## Remarks

An array index starts from 0.

## Examples

```pinescript
//@version=6
indicator("array.new_bool example")
length = 5
a = array.new_bool(length, close > open)
plot(array.get(a, 0) ? close : open)
```

## See also

- [array.new_float()](./new_float.md)
- [array.get()](./get.md)
- [array.slice()](./slice.md)
- [array.sort()](./sort.md)
