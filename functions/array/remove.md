---
title: "array.remove"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.remove
---

# array.remove

**Category:** Function

## Syntax

```pinescript
array.remove(id, index) → series <type>
```

## Description

The function changes the contents of an array by removing the element with the specified index.

## Arguments

- **`id`** `any array type` — An array object.
- **`index`** `series int` — The index of the element to remove.

## Returns

The value of the removed element.

## Remarks

If the index is positive, the function counts forwards from the beginning of the array to the end. The index of the first element is 0, and the index of the last element is `array.size() - 1`. If the index is negative, the function counts backwards from the end of the array to the beginning. In this case, the index of the last element is -1, and the index of the first element is negative `array.size()`. For example, for an array that contains three elements, all of the following are valid arguments for the `index` parameter: 0, 1, 2, -1, -2, -3.

## Examples

```pinescript
//@version=6
indicator("array.remove example")
a = array.new_float(5,high)
removedEl = array.remove(a, 0)
plot(array.size(a))
plot(removedEl)
```

## See also

- [array.new_float()](./new_float.md)
- [array.set()](./set.md)
- [array.push()](./push.md)
- [array.insert()](./insert.md)
- [array.pop()](./pop.md)
- [array.shift()](./shift.md)
