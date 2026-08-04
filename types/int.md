---
title: "int"
kind: type
source: https://www.tradingview.com/pine-script-reference/v6/#type_int
---

# int

**Category:** Type

## Description

Keyword used to explicitly declare the "int" (integer) type of a variable or a parameter.

## Remarks

Explicitly mentioning the type in a variable declaration is optional, except when it is initialized with [na](../variables/na.md). Learn more about Pine Script® types in the User Manual page on the [Type System](https://www.tradingview.com/pine-script-docs/language/type-system/).

## Examples

```pinescript
//@version=6
indicator("int")
int i = 14    // Same as `i = 14`
i := na
plot(i)
```

## See also

- [var](../keywords/var.md)
- [varip](../keywords/varip.md)
- [float](./float.md)
- [bool](./bool.md)
- [color](./color.md)
- [string](./string.md)
