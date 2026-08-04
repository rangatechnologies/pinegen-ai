---
title: "label.set_x"
kind: function
namespace: label
source: https://www.tradingview.com/pine-script-reference/v6/#fun_label.set_x
---

# label.set_x

**Category:** Function

## Syntax

```pinescript
label.set_x(id, x) → void
```

## Description

Sets bar index or bar time (depending on the xloc) of the label position.

## Arguments

- **`id`** `series label` — Label object.
- **`x`** `series int` — New bar index or bar time of the label position. Note that objects positioned using [xloc.bar_index](../../constants/xloc/bar_index.md) cannot be drawn further than 500 bars into the future.

**Return type(s):** `void`

## See also

- [label.new()](./new.md)
