---
title: "string"
kind: type
source: https://www.tradingview.com/pine-script-reference/v6/#type_string
---

# string

**Category:** Type

## Description

Keyword used to explicitly declare the "string" type of a variable or a parameter.

## Remarks

Explicitly mentioning the type in a variable declaration is optional, except when it is initialized with [na](../variables/na.md). Learn more about Pine Script® types in the User Manual page on the [Type System](https://www.tradingview.com/pine-script-docs/language/type-system/).

## Examples

```pinescript
//@version=6
indicator("string")
string s = "Hello World!"    // Same as `s = "Hello world!"`
// string s = na // same as ""
plot(na, title=s)
```

## See also

- [var](../keywords/var.md)
- [varip](../keywords/varip.md)
- [int](./int.md)
- [float](./float.md)
- [bool](./bool.md)
- [str.tostring()](../functions/str/tostring.md)
- [str.format()](../functions/str/format.md)
