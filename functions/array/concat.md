---
title: "array.concat"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.concat
---

# array.concat

**Category:** Function

## Syntax

```pinescript
array.concat(id1, id2) → array<type>
```

## Description

The function is used to merge two arrays. It pushes all elements from the second array to the first array, and returns the first array.

## Arguments

- **`id1`** `any array type` — The first array object.
- **`id2`** `any array type` — The second array object.

## Returns

The first array with merged elements from the second array.

## Examples

```pinescript
//@version=6
indicator("array.concat example")
a = array.new_float(0,0)
b = array.new_float(0,0)
for i = 0 to 4
    array.push(a, high[i])
    array.push(b, low[i])
c = array.concat(a,b)
plot(array.size(a))
plot(array.size(b))
plot(array.size(c))
```

## See also

- [array.new_float()](./new_float.md)
- [array.insert()](./insert.md)
- [array.slice()](./slice.md)
