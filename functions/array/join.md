---
title: "array.join"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.join
---

# array.join

**Category:** Function

## Syntax

```pinescript
array.join(id, separator) → series string
```

## Description

The function creates and returns a new string by concatenating all the elements of an array, separated by the specified separator string.

## Arguments

- **`id`** `array<int/float/string>` — An array object.
- **`separator`** `series string` (optional) — The string used to separate each array element.

**Return type(s):** `series string`

## Examples

```pinescript
//@version=6
indicator("array.join example")
a = array.new_float(5, 5)
label.new(bar_index, close, array.join(a, ","))
```

## See also

- [array.new_float()](./new_float.md)
- [array.set()](./set.md)
- [array.insert()](./insert.md)
- [array.remove()](./remove.md)
- [array.pop()](./pop.md)
- [array.unshift()](./unshift.md)
