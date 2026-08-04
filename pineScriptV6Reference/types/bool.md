---
title: "bool"
kind: type
source: https://www.tradingview.com/pine-script-reference/v6/#type_bool
---

# bool

**Category:** Type

## Description

Keyword used to explicitly declare the "bool" (boolean) type of a variable or a parameter. "Bool" variables can have values [true](../constants/true.md) or [false](../constants/false.md).

## Remarks

Explicitly mentioning the type in a variable declaration is optional. Learn more about Pine Script® types in the User Manual page on the [Type System](https://www.tradingview.com/pine-script-docs/language/type-system/).

## Examples

```pinescript
//@version=6
indicator("bool")
bool b = true    // Same as `b = true`
plot(b ? open : close)
```

## See also

- [var](../keywords/var.md)
- [varip](../keywords/varip.md)
- [int](./int.md)
- [float](./float.md)
- [color](./color.md)
- [string](./string.md)
- [true](../constants/true.md)
- [false](../constants/false.md)
