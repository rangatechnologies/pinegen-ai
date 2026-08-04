---
title: "ta.pivotlow"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.pivotlow
---

# ta.pivotlow

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
ta.pivotlow(leftbars, rightbars) → series float
```

```pinescript
ta.pivotlow(source, leftbars, rightbars) → series float
```

## Description

This function returns price of the pivot low point. It returns 'NaN', if there was no pivot low point.

## Arguments

- **`leftbars`** `series int/float` — Left strength.
- **`rightbars`** `series int/float` — Right strength.

## Returns

Price of the point or 'NaN'.

**Return type(s):** `series float`

## Remarks

If parameters 'leftbars' or 'rightbars' are series you should use [max_bars_back()](../max_bars_back.md) function for the 'source' variable.

## Examples

```pinescript
//@version=6
indicator("PivotLow", overlay=true)
leftBars = input(2)
rightBars=input(2)
pl = ta.pivotlow(close, leftBars, rightBars)
plot(pl, style=plot.style_cross, linewidth=3, color= color.blue, offset=-rightBars)
```
