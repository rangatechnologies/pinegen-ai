---
title: "array.copy"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.copy
---

# array.copy

**Category:** Function

## Syntax

```pinescript
array.copy(id) → array<type>
```

## Description

The function creates a copy of an existing array.

## Arguments

- **`id`** `any array type` — An array object.

## Returns

A copy of an array.

## Examples

```pinescript
//@version=6
indicator("array.copy example")
length = 5
a = array.new_float(length, close)
b = array.copy(a)
a := array.new_float(length, open)
plot(array.sum(a) / length)
plot(array.sum(b) / length)
```

## See also

- [array.new_float()](./new_float.md)
- [array.get()](./get.md)
- [array.slice()](./slice.md)
- [array.sort()](./sort.md)
