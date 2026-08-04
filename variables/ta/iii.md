---
title: "ta.iii"
kind: variable
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#var_ta.iii
---

# ta.iii

**Category:** Variable

**Type:** `series float`

## Description

Intraday Intensity Index.

## Examples

```pinescript
//@version=6
indicator("Intraday Intensity Index")
plot(ta.iii, color=color.yellow)

// the same on pine
f_iii() =>
    ((2 * close - high - low) / (high - low)) * volume

plot(f_iii())
```
