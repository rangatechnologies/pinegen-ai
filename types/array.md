---
title: "array"
kind: type
source: https://www.tradingview.com/pine-script-reference/v6/#type_array
---

# array

**Category:** Type

## Description

Keyword used to explicitly declare the "array" type of a variable or a parameter. Array objects (or IDs) can be created with the [array.new<type>()](../functions/array/new-type.md), [array.from()](../functions/array/from.md) function.

## Remarks

Array objects are always of "series" form.

## Examples

```pinescript
//@version=6
indicator("array", overlay=true)
array<float> a = na
a := array.new<float>(1, close)
plot(array.get(a, 0))
```

## See also

- [var](../keywords/var.md)
- [line](./line.md)
- [label](./label.md)
- [table](./table.md)
- [box](./box.md)
- [array.new<type>()](../functions/array/new-type.md)
- [array.from()](../functions/array/from.md)
