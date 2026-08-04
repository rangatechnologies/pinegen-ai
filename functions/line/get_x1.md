---
title: "line.get_x1"
kind: function
namespace: line
source: https://www.tradingview.com/pine-script-reference/v6/#fun_line.get_x1
---

# line.get_x1

**Category:** Function

## Syntax

```pinescript
line.get_x1(id) → series int
```

## Description

Returns UNIX time or bar index (depending on the last xloc value set) of the first point of the line.

## Arguments

- **`id`** `series line` — Line object.

## Returns

UNIX timestamp (in milliseconds) or bar index.

**Return type(s):** `series int`

## Examples

```pinescript
//@version=6
indicator("line.get_x1")
my_line = line.new(time, open, time + 60 * 60 * 24, close, xloc=xloc.bar_time)
a = line.get_x1(my_line)
plot(time - line.get_x1(my_line)) //draws zero plot
```

## See also

- [line.new()](./new.md)
