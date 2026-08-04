---
title: "line"
kind: type
source: https://www.tradingview.com/pine-script-reference/v6/#type_line
---

# line

**Category:** Type

## Description

Keyword used to explicitly declare the "line" type of a variable or a parameter. Line objects (or IDs) can be created with the [line.new()](../functions/line/new.md) function.

## Remarks

Line objects are always of "series" form.

## Examples

```pinescript
//@version=6
indicator("line")
// Empty `line1` line ID.
var line line1 = na
// `line` type is unnecessary because `line.new()` returns "line" type.
var line2 = line.new(na, na, na, na)
line3 = line.new(bar_index - 1, high, bar_index, high, extend = extend.right)
```

## See also

- [var](../keywords/var.md)
- [label](./label.md)
- [box](./box.md)
- [line.new()](../functions/line/new.md)
