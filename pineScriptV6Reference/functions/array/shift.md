---
title: "array.shift"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.shift
---

# array.shift

**Category:** Function

## Syntax

```pinescript
array.shift(id) → series <type>
```

## Description

The function removes an array's first element and returns its value.

## Arguments

- **`id`** `any array type` — An array object.

## Returns

The value of the removed element.

## Examples

```pinescript
//@version=6
indicator("array.shift example")
a = array.new_float(5,high)
removedEl = array.shift(a)
plot(array.size(a))
plot(removedEl)
```

## See also

- [array.unshift()](./unshift.md)
- [array.set()](./set.md)
- [array.push()](./push.md)
- [array.remove()](./remove.md)
- [array.includes()](./includes.md)
