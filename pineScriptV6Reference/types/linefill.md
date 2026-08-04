---
title: "linefill"
kind: type
source: https://www.tradingview.com/pine-script-reference/v6/#type_linefill
---

# linefill

**Category:** Type

## Description

Keyword used to explicitly declare the "linefill" type of a variable or a parameter. Linefill objects (or IDs) can be created with the [linefill.new()](../functions/linefill/new.md) function.

## Remarks

Linefill objects are always of "series" form.

## Examples

```pinescript
//@version=6
indicator("linefill", overlay=true)
// Empty `linefill1` line ID.
var linefill linefill1 = na
// `linefill` type is unnecessary because `linefill.new()` returns "linefill" type.
var linefill2 = linefill.new(na, na, na)

if barstate.islastconfirmedhistory
	line1 = line.new(bar_index - 10, high+1, bar_index, high+1, extend = extend.right)
	line2 = line.new(bar_index - 10, low+1, bar_index, low+1, extend = extend.right)
	linefill3 = linefill.new(line1, line2, color = color.new(color.green, 80))
```

## See also

- [var](../keywords/var.md)
- [line](./line.md)
- [label](./label.md)
- [table](./table.md)
- [box](./box.md)
- [linefill.new()](../functions/linefill/new.md)
