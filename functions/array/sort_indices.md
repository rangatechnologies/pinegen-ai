---
title: "array.sort_indices"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.sort_indices
---

# array.sort_indices

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
array.sort_indices(id, order) → array<int>
```

```pinescript
array.sort_indices(id, order, sort_field) → array<int>
```

## Description

Returns an array of indices which, when used to index the original array, will access its elements in their sorted order. It does not modify the original array.

## Arguments

- **`id`** `array<int/float/string>` — An array object.
- **`order`** `series sort_order` (optional) — The sort order: order.ascending or order.descending. Optional. The default is order.ascending.

**Return type(s):** `array<int>`

## Examples

```pinescript
//@version=6
indicator("array.sort_indices")
a = array.from(5, -2, 0, 9, 1)
sortedIndices = array.sort_indices(a) // [1, 2, 4, 0, 3]
indexOfSmallestValue = array.get(sortedIndices, 0) // 1
smallestValue = array.get(a, indexOfSmallestValue) // -2
plot(smallestValue)
```

## See also

- [array.new_float()](./new_float.md)
- [array.insert()](./insert.md)
- [array.slice()](./slice.md)
- [array.reverse()](./reverse.md)
- [order.ascending](../../constants/order/ascending.md)
- [order.descending](../../constants/order/descending.md)
