---
title: "array.indexof"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.indexof
---

# array.indexof

**Category:** Function

## Syntax

```pinescript
array.indexof(id, value) → series int
```

## Description

The function returns the index of the first occurrence of the value, or -1 if the value is not found.

## Arguments

- **`id`** `any array type` — An array object.
- **`value`** `series <type of the array's elements>` — The value to search in the array.

## Returns

The index of an element.

**Return type(s):** `series int`

## Examples

```pinescript
//@version=6
indicator("array.indexof example")
a = array.new_float(5,high)
index = array.indexof(a, high)
plot(index)
```

## See also

- [array.lastindexof()](./lastindexof.md)
- [array.get()](./get.md)
- [array.lastindexof()](./lastindexof.md)
- [array.remove()](./remove.md)
- [array.insert()](./insert.md)
