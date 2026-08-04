---
title: "array.size"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.size
---

# array.size

**Category:** Function

## Syntax

```pinescript
array.size(id) → series int
```

## Description

The function returns the number of elements in an array.

## Arguments

- **`id`** `any array type` — An array object.

## Returns

The number of elements in the array.

**Return type(s):** `series int`

## Examples

```pinescript
//@version=6
indicator("array.size example")
a = array.new_float(0)
for i = 0 to 9
	array.push(a, close[i])
// note that changes in slice also modify original array
slice = array.slice(a, 0, 5)
array.push(slice, open)
// size was changed in slice and in original array
plot(array.size(a))
plot(array.size(slice))
```

## See also

- [array.new_float()](./new_float.md)
- [array.sum()](./sum.md)
- [array.slice()](./slice.md)
- [array.sort()](./sort.md)
