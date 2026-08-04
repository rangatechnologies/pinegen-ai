---
title: "line.set_xy1"
kind: function
namespace: line
source: https://www.tradingview.com/pine-script-reference/v6/#fun_line.set_xy1
---

# line.set_xy1

**Category:** Function

## Syntax

```pinescript
line.set_xy1(id, x, y) → void
```

## Description

Sets bar index/time and price of the first point.

## Arguments

- **`id`** `series line` — Line object.
- **`x`** `series int` — Bar index or bar time. Note that objects positioned using [xloc.bar_index](../../constants/xloc/bar_index.md) cannot be drawn further than 500 bars into the future.
- **`y`** `series int/float` — Price.

**Return type(s):** `void`

## See also

- [line.new()](./new.md)
