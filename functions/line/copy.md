---
title: "line.copy"
kind: function
namespace: line
source: https://www.tradingview.com/pine-script-reference/v6/#fun_line.copy
---

# line.copy

**Category:** Function

## Syntax

```pinescript
line.copy(id) → series line
```

## Description

Clones the line object.

## Arguments

- **`id`** `series line` — Line object.

## Returns

New line ID object which may be passed to line.setXXX and line.getXXX functions.

**Return type(s):** `series line`

## Examples

```pinescript
//@version=6
indicator('Last 100 bars price range', overlay = true)
LOOKBACK = 100
highest = ta.highest(LOOKBACK)
lowest = ta.lowest(LOOKBACK)
if barstate.islastconfirmedhistory
	var lineTop = line.new(bar_index[LOOKBACK], highest, bar_index, highest, color = color.green)
	var lineBottom = line.copy(lineTop)
	line.set_y1(lineBottom, lowest)
	line.set_y2(lineBottom, lowest)
	line.set_color(lineBottom, color.red)
```

## See also

- [line.new()](./new.md)
- [line.delete()](./delete.md)
