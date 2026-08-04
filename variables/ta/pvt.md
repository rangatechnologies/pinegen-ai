---
title: "ta.pvt"
kind: variable
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#var_ta.pvt
---

# ta.pvt

**Category:** Variable

**Type:** `series float`

## Description

Price-Volume Trend.

## Examples

```pinescript
//@version=6
indicator("Price-Volume Trend")
plot(ta.pvt, color=color.yellow)

// the same on pine
f_pvt() =>
    ta.cum((ta.change(close) / close[1]) * volume)

plot(f_pvt())
```
