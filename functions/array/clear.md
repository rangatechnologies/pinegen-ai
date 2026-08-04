---
title: "array.clear"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.clear
---

# array.clear

**Category:** Function

## Syntax

```pinescript
array.clear(id) → void
```

## Description

The function removes all elements from an array.

## Arguments

- **`id`** `any array type` — An array object.

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
indicator("array.clear example")
a = array.new_float(5,high)
array.clear(a)
array.push(a, close)
plot(array.get(a,0))
plot(array.size(a))
```

## See also

- [array.new_float()](./new_float.md)
- [array.insert()](./insert.md)
- [array.push()](./push.md)
- [array.remove()](./remove.md)
- [array.pop()](./pop.md)
