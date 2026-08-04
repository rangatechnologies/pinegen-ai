---
title: "linefill.new"
kind: function
namespace: linefill
source: https://www.tradingview.com/pine-script-reference/v6/#fun_linefill.new
---

# linefill.new

**Category:** Function

## Syntax

```pinescript
linefill.new(line1, line2, color) → series linefill
```

## Description

Creates a new linefill object and displays it on the chart, filling the space between `line1` and `line2` with the color specified in `color`.

## Arguments

- **`line1`** `series line` — First line object.
- **`line2`** `series line` — Second line object.
- **`color`** `series color` — The color used to fill the space between the lines.

## Returns

The ID of a linefill object that can be passed to other linefill.*() functions.

**Return type(s):** `series linefill`

## Remarks

If any line of the two is deleted, the linefill object is also deleted. If the lines are moved (e.g. via [line.set_xy()](https://www.tradingview.com/pine-script-reference/v6/#fun_line.set_xy) functions), the linefill object is also moved.

If both lines are extended in the same direction relative to the lines themselves (e.g. both have [extend.right](../../constants/extend/right.md) as the value of their `extend=` parameter), the space between line extensions will also be filled.
