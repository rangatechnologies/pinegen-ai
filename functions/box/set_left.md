---
title: "box.set_left"
kind: function
namespace: box
source: https://www.tradingview.com/pine-script-reference/v6/#fun_box.set_left
---

# box.set_left

**Category:** Function

## Syntax

```pinescript
box.set_left(id, left) → void
```

## Description

Sets the left coordinate of the box.

## Arguments

- **`id`** `series box` — A box object.
- **`left`** `series int` — Bar index or bar time of the left border. Note that objects positioned using [xloc.bar_index](../../constants/xloc/bar_index.md) cannot be drawn further than 500 bars into the future.

**Return type(s):** `void`

## See also

- [box.new()](./new.md)
- [box.get_left()](./get_left.md)
