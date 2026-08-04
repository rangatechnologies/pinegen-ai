---
title: "array.last"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.last
---

# array.last

**Category:** Function

## Syntax

```pinescript
array.last(id) → series <type>
```

## Description

Returns the array's last element. Throws a runtime error if the array is empty.

## Arguments

- **`id`** `any array type` — An array object.

## Examples

```pinescript
//@version=6
indicator("array.last example")
arr = array.new_int(3, 10)
plot(array.last(arr))
```

## See also

- [array.first()](./first.md)
- [array.get()](./get.md)
