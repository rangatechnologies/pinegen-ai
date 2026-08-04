---
title: "line.get_x2"
kind: function
namespace: line
source: https://www.tradingview.com/pine-script-reference/v6/#fun_line.get_x2
---

# line.get_x2

**Category:** Function

## Syntax

```pinescript
line.get_x2(id) → series int
```

## Description

Returns UNIX time or bar index (depending on the last xloc value set) of the second point of the line.

## Arguments

- **`id`** `series line` — Line object.

## Returns

UNIX timestamp (in milliseconds) or bar index.

**Return type(s):** `series int`

## See also

- [line.new()](./new.md)
