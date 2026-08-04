---
title: "float"
kind: type
source: https://www.tradingview.com/pine-script-reference/v6/#type_float
---

# float

**Category:** Type

## Description

Keyword used to explicitly declare the "float" (floating point) type of a variable or a parameter.

## Remarks

Explicitly mentioning the type in a variable declaration is optional, except when it is initialized with [na](../variables/na.md). Learn more about Pine Script® types in the User Manual page on the [Type System](https://www.tradingview.com/pine-script-docs/language/type-system/).

## Examples

```pinescript
//@version=6
indicator("float")
float f = 3.14    // Same as `f = 3.14`
f := na
plot(f)
```

## See also

- [var](../keywords/var.md)
- [varip](../keywords/varip.md)
- [int](./int.md)
- [bool](./bool.md)
- [color](./color.md)
- [string](./string.md)
