---
title: "array.binary_search"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.binary_search
---

# array.binary_search

**Category:** Function

## Syntax

```pinescript
array.binary_search(id, val) → series int
```

## Description

The function returns the index of the value, or -1 if the value is not found. The array to search must be sorted in ascending order.

## Arguments

- **`id`** `array<int/float>` — An array object.
- **`val`** `series int/float` — The value to search for in the array.

**Return type(s):** `series int`

## Remarks

A binary search works on arrays pre-sorted in ascending order. It begins by comparing an element in the middle of the array with the target value. If the element matches the target value, its position in the array is returned. If the element's value is greater than the target value, the search continues in the lower half of the array. If the element's value is less than the target value, the search continues in the upper half of the array. By doing this recursively, the algorithm progressively eliminates smaller and smaller portions of the array in which the target value cannot lie.

## Examples

```pinescript
//@version=6
indicator("array.binary_search")
a = array.from(5, -2, 0, 9, 1)
array.sort(a) // [-2, 0, 1, 5, 9]
position = array.binary_search(a, 0) // 1
plot(position)
```

## See also

- [array.new_float()](./new_float.md)
- [array.insert()](./insert.md)
- [array.slice()](./slice.md)
- [array.reverse()](./reverse.md)
- [order.ascending](../../constants/order/ascending.md)
- [order.descending](../../constants/order/descending.md)
