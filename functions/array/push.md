---
title: "array.push"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.push
---

# array.push

**Category:** Function

## Syntax

```pinescript
array.push(id, value) → void
```

## Description

The function appends a value to an array.

## Arguments

- **`id`** `any array type` — An array object.
- **`value`** `series <type of the array's elements>` — The value of the element added to the end of the array.

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
indicator("array.push example")
a = array.new_float(5, 0)
array.push(a, open)
plot(array.get(a, 5))
```

## See also

- [array.new_float()](./new_float.md)
- [array.set()](./set.md)
- [array.insert()](./insert.md)
- [array.remove()](./remove.md)
- [array.pop()](./pop.md)
- [array.unshift()](./unshift.md)
