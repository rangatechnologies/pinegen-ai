---
title: "line.set_x2"
kind: function
namespace: line
source: https://www.tradingview.com/pine-script-reference/v6/#fun_line.set_x2
---

# line.set_x2

**Category:** Function

## Syntax

```pinescript
line.set_x2(id, x) → void
```

## Description

Sets bar index or bar time (depending on the xloc) of the second point.

## Arguments

- **`id`** `series line` — Line object.
- **`x`** `series int` — Bar index or bar time. Note that objects positioned using [xloc.bar_index](../../constants/xloc/bar_index.md) cannot be drawn further than 500 bars into the future.

**Return type(s):** `void`

## See also

- [line.new()](./new.md)
