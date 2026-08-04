---
title: "array.set"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.set
---

# array.set

**Category:** Function

## Syntax

```pinescript
array.set(id, index, value) → void
```

## Description

The function sets the value of the element at the specified index.

## Arguments

- **`id`** `any array type` — An array object.
- **`index`** `series int` — The index of the element to be modified.
- **`value`** `series <type of the array's elements>` — The new value to be set.

**Return type(s):** `void`

## Remarks

If the index is positive, the function counts forwards from the beginning of the array to the end. The index of the first element is 0, and the index of the last element is `array.size() - 1`. If the index is negative, the function counts backwards from the end of the array to the beginning. In this case, the index of the last element is -1, and the index of the first element is negative `array.size()`. For example, for an array that contains three elements, all of the following are valid arguments for the `index` parameter: 0, 1, 2, -1, -2, -3.

## Examples

```pinescript
//@version=6
indicator("array.set example")
a = array.new_float(10)
for i = 0 to 9
	array.set(a, i, close[i])
plot(array.sum(a) / 10)
```

## See also

- [array.new_float()](./new_float.md)
- [array.get()](./get.md)
- [array.slice()](./slice.md)
