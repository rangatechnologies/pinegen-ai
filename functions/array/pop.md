---
title: "array.pop"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.pop
---

# array.pop

**Category:** Function

## Syntax

```pinescript
array.pop(id) → series <type>
```

## Description

The function removes the last element from an array and returns its value.

## Arguments

- **`id`** `any array type` — An array object.

## Returns

The value of the removed element.

## Examples

```pinescript
//@version=6
indicator("array.pop example")
a = array.new_float(5,high)
removedEl = array.pop(a)
plot(array.size(a))
plot(removedEl)
```

## See also

- [array.new_float()](./new_float.md)
- [array.set()](./set.md)
- [array.push()](./push.md)
- [array.remove()](./remove.md)
- [array.insert()](./insert.md)
- [array.shift()](./shift.md)
