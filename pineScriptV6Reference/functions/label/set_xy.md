---
title: "label.set_xy"
kind: function
namespace: label
source: https://www.tradingview.com/pine-script-reference/v6/#fun_label.set_xy
---

# label.set_xy

**Category:** Function

## Syntax

```pinescript
label.set_xy(id, x, y) → void
```

## Description

Sets bar index/time and price of the label position.

## Arguments

- **`id`** `series label` — Label object.
- **`x`** `series int` — New bar index or bar time of the label position. Note that objects positioned using [xloc.bar_index](../../constants/xloc/bar_index.md) cannot be drawn further than 500 bars into the future.
- **`y`** `series int/float` — New price of the label position.

**Return type(s):** `void`

## See also

- [label.new()](./new.md)
