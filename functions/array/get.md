---
title: "array.get"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.get
---

# array.get

**Category:** Function

## Syntax

```pinescript
array.get(id, index) → series <type>
```

## Description

The function returns the value of the element at the specified index.

## Arguments

- **`id`** `any array type` — An array object.
- **`index`** `series int` — The index of the element whose value is to be returned.

## Returns

The array element's value.

## Remarks

If the index is positive, the function counts forwards from the beginning of the array to the end. The index of the first element is 0, and the index of the last element is `array.size() - 1`. If the index is negative, the function counts backwards from the end of the array to the beginning. In this case, the index of the last element is -1, and the index of the first element is negative `array.size()`. For example, for an array that contains three elements, all of the following are valid arguments for the `index` parameter: 0, 1, 2, -1, -2, -3.

## Examples

```pinescript
//@version=6
indicator("array.get example")
a = array.new_float(0)
for i = 0 to 9
	array.push(a, close[i] - open[i])
plot(array.get(a, 9))
```

## See also

- [array.new_float()](./new_float.md)
- [array.set()](./set.md)
- [array.slice()](./slice.md)
- [array.sort()](./sort.md)
