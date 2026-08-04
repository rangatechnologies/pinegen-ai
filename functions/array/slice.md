---
title: "array.slice"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.slice
---

# array.slice

**Category:** Function

## Syntax

```pinescript
array.slice(id, index_from, index_to) → array<type>
```

## Description

Creates an array representing a slice of an existing array. Setting a slice's element to a new value changes the corresponding element in the original array to that value. Likewise, inserting or removing an element in the slice inserts or removes an element in the original array at the index range covered by the slice.

## Arguments

- **`id`** `any array type` — The reference (ID) of the array from which to create a new slice.
- **`index_from`** `series int` (optional) — The `id` array index corresponding to the start of the slice.
- **`index_to`** `series int` (optional) — The `id` array index corresponding to the end of the slice. The index is non-inclusive; the resulting slice contains all the original array's elements from `index_from` to `index_to - 1`.

## Returns

The ID of an array representing a slice of the `id` array.

## Remarks

The indices in the resulting slice range from zero to one less than the slice's size. These indices do not directly represent the same element indices as the original array. For example, if the `index_from` value is 5, the slice's element at index 1 refers to the `id` array's element at index 6.



Scripts cannot modify the elements of a historical array. Therefore, they cannot modify historical array slices created by this function. Instead of modifying an array referenced by an ID retrieved with the [[]](../../operators/history-reference.md) operator, use [array.copy()](./copy.md) to create a shallow copy of the historical array, then modify the copy or a slice of that copy instead.

## Examples

```pinescript
//@version=6
indicator("array.slice example")
a = array.new_float(0)
for i = 0 to 9
	array.push(a, close[i])
// take elements from 0 to 4
// *note that changes in slice also modify original array
slice = array.slice(a, 0, 5)
plot(array.sum(a) / 10)
plot(array.sum(slice) / 5)
```

## See also

- [array.new_float()](./new_float.md)
- [array.get()](./get.md)
- [array.sort()](./sort.md)
