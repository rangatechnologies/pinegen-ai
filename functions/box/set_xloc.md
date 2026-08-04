---
title: "box.set_xloc"
kind: function
namespace: box
source: https://www.tradingview.com/pine-script-reference/v6/#fun_box.set_xloc
---

# box.set_xloc

**Category:** Function

## Syntax

```pinescript
box.set_xloc(id, left, right, xloc) → void
```

## Description

Sets the left and right borders of a [box](../../types/box.md) and updates its `xloc` property.

## Arguments

- **`id`** `series box` — The ID of the box object to update.
- **`left`** `series int` — The bar index or timestamp for the left border of the box.
- **`right`** `series int` — The bar index or timestamp for the right border of the box.
- **`xloc`** `series string` — Determines whether the box treats the `left` and `right` arguments as bar indices or timestamps. Possible values: [xloc.bar_index](../../constants/xloc/bar_index.md) and [xloc.bar_time](../../constants/xloc/bar_time.md). If the value is [xloc.bar_index](../../constants/xloc/bar_index.md), the arguments represent bar indices. If [xloc.bar_time](../../constants/xloc/bar_time.md), the arguments represent [UNIX timestamps](https://www.tradingview.com/pine-script-docs/concepts/time/#unix-timestamps).

**Return type(s):** `void`

## See also

- [box.new()](./new.md)
- [xloc.bar_index](../../constants/xloc/bar_index.md)
- [xloc.bar_time](../../constants/xloc/bar_time.md)
