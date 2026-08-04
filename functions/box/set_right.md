---
title: "box.set_right"
kind: function
namespace: box
source: https://www.tradingview.com/pine-script-reference/v6/#fun_box.set_right
---

# box.set_right

**Category:** Function

## Syntax

```pinescript
box.set_right(id, right) → void
```

## Description

Sets the right coordinate of the box.

## Arguments

- **`id`** `series box` — A box object.
- **`right`** `series int` — Bar index or bar time of the right border. Note that objects positioned using [xloc.bar_index](../../constants/xloc/bar_index.md) cannot be drawn further than 500 bars into the future.

**Return type(s):** `void`

## See also

- [box.new()](./new.md)
- [box.get_right()](./get_right.md)
