---
title: "array.unshift"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.unshift
---

# array.unshift

**Category:** Function

## Syntax

```pinescript
array.unshift(id, value) → void
```

## Description

The function inserts the value at the beginning of the array.

## Arguments

- **`id`** `any array type` — An array object.
- **`value`** `series <type of the array's elements>` — The value to add to the start of the array.

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
indicator("array.unshift example")
a = array.new_float(5, 0)
array.unshift(a, open)
plot(array.get(a, 0))
```

## See also

- [array.shift()](./shift.md)
- [array.set()](./set.md)
- [array.insert()](./insert.md)
- [array.remove()](./remove.md)
- [array.indexof()](./indexof.md)
