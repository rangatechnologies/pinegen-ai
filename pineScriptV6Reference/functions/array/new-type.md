---
title: "array.new<type>"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.new<type>
---

# array.new<type>

**Category:** Function

## Syntax

```pinescript
array.new<type>(size, initial_value) → array<type>
```

## Description

The function creates a new array object of <type> elements.

## Arguments

- **`size`** `series int` (optional) — Initial size of an array. Optional. The default is 0.
- **`initial_value`** `<array_type>` (optional) — Initial value of all array elements. Optional. The default is 'na'.

## Returns

The ID of an array object which may be used in other array.*() functions.

## Remarks

An array index starts from 0.

If you want to initialize an array and specify all its elements at the same time, then use the function array.from.

## Detailed Description



```pinescript
//@version=6
indicator("array.new<color> example")
a = array.new<color>()
array.push(a, color.red)
array.push(a, color.green)
plot(close, color = array.get(a, close > open ? 1 : 0))
```

---



```pinescript
//@version=6
indicator("array.new<float> example")
length = 5
var a = array.new<float>(length, close)
if array.size(a) == length
	array.remove(a, 0)
	array.push(a, close)
plot(array.sum(a) / length, "SMA")
```

---



```pinescript
//@version=6
indicator("array.new<line> example")
// draw last 15 lines
var a = array.new<line>()
array.push(a, line.new(bar_index - 1, close[1], bar_index, close))
if array.size(a) > 15
    ln = array.shift(a)
    line.delete(ln)
```

## Examples

```pinescript
//@version=6
indicator("array.new<string> example")
a = array.new<string>(1, "Hello, World!")
label.new(bar_index, close, array.get(a, 0))
```

## See also

- [array.from()](./from.md)
- [array.push()](./push.md)
- [array.get()](./get.md)
- [array.size()](./size.md)
- [array.remove()](./remove.md)
- [array.shift()](./shift.md)
- [array.sum()](./sum.md)
