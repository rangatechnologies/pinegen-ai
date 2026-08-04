---
title: "label.set_xloc"
kind: function
namespace: label
source: https://www.tradingview.com/pine-script-reference/v6/#fun_label.set_xloc
---

# label.set_xloc

**Category:** Function

## Syntax

```pinescript
label.set_xloc(id, x, xloc) → void
```

## Description

Sets x-location and new bar index/time value.

## Arguments

- **`id`** `series label` — Label object.
- **`x`** `series int` — New bar index or bar time of the label position.
- **`xloc`** `series string` — New x-location value.

**Return type(s):** `void`

## See also

- [xloc.bar_index](../../constants/xloc/bar_index.md)
- [xloc.bar_time](../../constants/xloc/bar_time.md)
- [label.new()](./new.md)
