---
title: "ta.pivothigh"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.pivothigh
---

# ta.pivothigh

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
ta.pivothigh(leftbars, rightbars) → series float
```

```pinescript
ta.pivothigh(source, leftbars, rightbars) → series float
```

## Description

This function returns price of the pivot high point. It returns 'NaN', if there was no pivot high point.

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
indicator("PivotHigh", overlay=true)
leftBars = input(2)
rightBars=input(2)
ph = ta.pivothigh(leftBars, rightBars)
plot(ph, style=plot.style_cross, linewidth=3, color= color.red, offset=-rightBars)
```
