---
title: "box"
kind: type
source: https://www.tradingview.com/pine-script-reference/v6/#type_box
---

# box

**Category:** Type

## Description

Keyword used to explicitly declare the "box" type of a variable or a parameter. Box objects (or IDs) can be created with the [box.new()](../functions/box/new.md) function.

## Remarks

Box objects are always of "series" form.

## Examples

```pinescript
//@version=6
indicator("box")
// Empty `box1` box ID.
var box box1 = na
// `box` type is unnecessary because `box.new()` returns a "box" type.
var box2 = box.new(na, na, na, na)
box3 = box.new(time, open, time + 60 * 60 * 24, close, xloc=xloc.bar_time)
```

## See also

- [var](../keywords/var.md)
- [line](./line.md)
- [label](./label.md)
- [table](./table.md)
- [box.new()](../functions/box/new.md)
