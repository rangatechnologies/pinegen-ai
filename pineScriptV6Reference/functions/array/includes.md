---
title: "array.includes"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.includes
---

# array.includes

**Category:** Function

## Syntax

```pinescript
array.includes(id, value) → series bool
```

## Description

The function returns true if the value was found in an array, false otherwise.

## Arguments

- **`id`** `any array type` — An array object.
- **`value`** `series <type of the array's elements>` — The value to search in the array.

## Returns

True if the value was found in the array, false otherwise.

**Return type(s):** `series bool`

## Examples

```pinescript
//@version=6
indicator("array.includes example")
a = array.new_float(5,high)
p = close
if array.includes(a, high)
	p := open
plot(p)
```

## See also

- [array.new_float()](./new_float.md)
- [array.indexof()](./indexof.md)
- [array.shift()](./shift.md)
- [array.remove()](./remove.md)
- [array.insert()](./insert.md)
