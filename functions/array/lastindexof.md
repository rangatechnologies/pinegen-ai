---
title: "array.lastindexof"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.lastindexof
---

# array.lastindexof

**Category:** Function

## Syntax

```pinescript
array.lastindexof(id, value) → series int
```

## Description

The function returns the index of the last occurrence of the value, or -1 if the value is not found.

## Arguments

- **`id`** `any array type` — An array object.
- **`value`** `series <type of the array's elements>` — The value to search in the array.

## Returns

The index of an element.

**Return type(s):** `series int`

## Examples

```pinescript
//@version=6
indicator("array.lastindexof example")
a = array.new_float(5,high)
index = array.lastindexof(a, high)
plot(index)
```

## See also

- [array.new_float()](./new_float.md)
- [array.set()](./set.md)
- [array.push()](./push.md)
- [array.remove()](./remove.md)
- [array.insert()](./insert.md)
