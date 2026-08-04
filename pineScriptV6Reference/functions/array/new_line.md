---
title: "array.new_line"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.new_line
---

# array.new_line

**Category:** Function

## Syntax

```pinescript
array.new_line(size, initial_value) → array<line>
```

## Description

The function creates a new array object of line type elements.

## Arguments

- **`size`** `series int` (optional) — Initial size of an array. Optional. The default is 0.
- **`initial_value`** `series line` (optional) — Initial value of all array elements. Optional. The default is 'na'.

## Returns

The ID of an array object which may be used in other array.*() functions.

**Return type(s):** `array<line>`

## Remarks

An array index starts from 0.

## Examples

```pinescript
//@version=6
indicator("array.new_line example")
// draw last 15 lines
var a = array.new_line()
array.push(a, line.new(bar_index - 1, close[1], bar_index, close))
if array.size(a) > 15
	ln = array.shift(a)
	line.delete(ln)
```

## See also

- [array.new_float()](./new_float.md)
- [array.get()](./get.md)
- [array.slice()](./slice.md)
