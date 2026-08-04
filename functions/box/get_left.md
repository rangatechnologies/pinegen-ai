---
title: "box.get_left"
kind: function
namespace: box
source: https://www.tradingview.com/pine-script-reference/v6/#fun_box.get_left
---

# box.get_left

**Category:** Function

## Syntax

```pinescript
box.get_left(id) → series int
```

## Description

Returns the bar index or the UNIX time (depending on the last value used for 'xloc') of the left border of the box.

## Arguments

- **`id`** `series box` — A box object.

## Returns

A bar index or a UNIX timestamp (in milliseconds).

**Return type(s):** `series int`

## See also

- [box.new()](./new.md)
- [box.set_left()](./set_left.md)
