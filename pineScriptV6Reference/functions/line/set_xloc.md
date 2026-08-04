---
title: "line.set_xloc"
kind: function
namespace: line
source: https://www.tradingview.com/pine-script-reference/v6/#fun_line.set_xloc
---

# line.set_xloc

**Category:** Function

## Syntax

```pinescript
line.set_xloc(id, x1, x2, xloc) → void
```

## Description

Sets x-location and new bar index/time values.

## Arguments

- **`id`** `series line` — Line object.
- **`x1`** `series int` — Bar index or bar time of the first point.
- **`x2`** `series int` — Bar index or bar time of the second point.
- **`xloc`** `series string` — New x-location value.

**Return type(s):** `void`

## See also

- [xloc.bar_index](../../constants/xloc/bar_index.md)
- [xloc.bar_time](../../constants/xloc/bar_time.md)
- [line.new()](./new.md)
