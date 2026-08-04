---
title: "box.get_right"
kind: function
namespace: box
source: https://www.tradingview.com/pine-script-reference/v6/#fun_box.get_right
---

# box.get_right

**Category:** Function

## Syntax

```pinescript
box.get_right(id) → series int
```

## Description

Returns the bar index or the UNIX time (depending on the last value used for 'xloc') of the right border of the box.

## Arguments

- **`id`** `series box` — A box object.

## Returns

A bar index or a UNIX timestamp (in milliseconds).

**Return type(s):** `series int`

## See also

- [box.new()](./new.md)
- [box.set_right()](./set_right.md)
