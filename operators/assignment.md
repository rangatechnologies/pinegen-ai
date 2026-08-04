---
title: "="
kind: operator
source: https://www.tradingview.com/pine-script-reference/v6/#op_=
---

# =

**Category:** Operator

## Syntax

```pinescript
<var_name> := <initial_value>
```

## Description

Assignment operator. Assigns an initial value or reference to a declared variable. It means *this is a new variable, and it starts with this value*.

## Examples

```pinescript
//@version=6
indicator("`=` showcase")
// The following are all valid variable declarations.
i = 1
MS_IN_ONE_MINUTE = 1000 * 60
showPlotInput = input.bool(true, "Show plots")
pHi = ta.pivothigh(5, 5)
plotColor = color.green

plot(pHi, color = plotColor, display = showPlotInput ? display.all : display.none, precision = i)
```
