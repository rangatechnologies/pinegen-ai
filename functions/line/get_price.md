---
title: "line.get_price"
kind: function
namespace: line
source: https://www.tradingview.com/pine-script-reference/v6/#fun_line.get_price
---

# line.get_price

**Category:** Function

## Syntax

```pinescript
line.get_price(id, x) → series float
```

## Description

Returns the price level of a line at a given bar index.

## Arguments

- **`id`** `series line` — Line object.
- **`x`** `series int` — Bar index for which price is required.

## Returns

Price value of line 'id' at bar index 'x'.

**Return type(s):** `series float`

## Remarks

The line is considered to have been created using 'extend=extend.both'.

This function can only be called for lines created using 'xloc.bar_index'. If you try to call it for a line created with 'xloc.bar_time', it will generate an error.

## Examples

```pinescript
//@version=6
indicator("GetPrice", overlay=true)
var line l = na
if bar_index == 10
    l := line.new(0, high[5], bar_index, high)
plot(line.get_price(l, bar_index), color=color.green)
```

## See also

- [line.new()](./new.md)
