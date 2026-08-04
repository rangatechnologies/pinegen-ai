---
title: "label"
kind: type
source: https://www.tradingview.com/pine-script-reference/v6/#type_label
---

# label

**Category:** Type

## Description

Keyword used to explicitly declare the "label" type of a variable or a parameter. Label objects (or IDs) can be created with the [label.new()](../functions/label/new.md) function.

## Remarks

Label objects are always of "series" form.

## Examples

```pinescript
//@version=6
indicator("label")
// Empty `label1` label ID.
var label label1 = na
// `label` type is unnecessary because `label.new()` returns "label" type.
var label2 = label.new(na, na, na)
if barstate.islastconfirmedhistory
	label3 = label.new(bar_index, high, text = "label3 text")
```

## See also

- [var](../keywords/var.md)
- [line](./line.md)
- [box](./box.md)
- [label.new()](../functions/label/new.md)
