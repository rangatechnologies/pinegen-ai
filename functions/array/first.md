---
title: "array.first"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.first
---

# array.first

**Category:** Function

## Syntax

```pinescript
array.first(id) → series <type>
```

## Description

Returns the array's first element. Throws a runtime error if the array is empty.

## Arguments

- **`id`** `any array type` — An array object.

## Examples

```pinescript
//@version=6
indicator("array.first example")
arr = array.new_int(3, 10)
plot(array.first(arr))
```

## See also

- [array.last()](./last.md)
- [array.get()](./get.md)
