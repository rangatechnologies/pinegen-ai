---
title: "array.fill"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.fill
---

# array.fill

**Category:** Function

## Syntax

```pinescript
array.fill(id, value, index_from, index_to) → void
```

## Description

The function sets elements of an array to a single value. If no index is specified, all elements are set. If only a start index (default 0) is supplied, the elements starting at that index are set. If both index parameters are used, the elements from the starting index up to but not including the end index (default na) are set.

## Arguments

- **`id`** `any array type` — An array object.
- **`value`** `series <type of the array's elements>` — Value to fill the array with.
- **`index_from`** `series int` (optional) — Start index, default is 0.
- **`index_to`** `series int` (optional) — End index, default is na. Must be one greater than the index of the last element to set.

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
indicator("array.fill example")
a = array.new_float(10)
array.fill(a, close)
plot(array.sum(a))
```

## See also

- [array.new_float()](./new_float.md)
- [array.set()](./set.md)
- [array.slice()](./slice.md)
