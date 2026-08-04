---
title: "array.insert"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.insert
---

# array.insert

**Category:** Function

## Syntax

```pinescript
array.insert(id, index, value) → void
```

## Description

The function changes the contents of an array by adding new elements in place.

## Arguments

- **`id`** `any array type` — An array object.
- **`index`** `series int` (optional) — The index at which to insert the value.
- **`value`** `series <type of the array's elements>` — The value to add to the array.

**Return type(s):** `void`

## Remarks

If the index is positive, the function counts forwards from the beginning of the array to the end. The index of the first element is 0, and the index of the last element is `array.size() - 1`. If the index is negative, the function counts backwards from the end of the array to the beginning. In this case, the index of the last element is -1, and the index of the first element is negative `array.size()`. For example, for an array that contains three elements, all of the following are valid arguments for the `index` parameter: 0, 1, 2, -1, -2, -3.

## Examples

```pinescript
//@version=6
indicator("array.insert example")
a = array.new_float(5, close)
array.insert(a, 0, open)
plot(array.get(a, 5))
```

## See also

- [array.new_float()](./new_float.md)
- [array.set()](./set.md)
- [array.push()](./push.md)
- [array.remove()](./remove.md)
- [array.pop()](./pop.md)
- [array.unshift()](./unshift.md)
