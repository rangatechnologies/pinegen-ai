---
title: "ta.wvad"
kind: variable
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#var_ta.wvad
---

# ta.wvad

**Category:** Variable

**Type:** `series float`

## Description

Williams Variable Accumulation/Distribution.

## Examples

```pinescript
//@version=6
indicator("Williams Variable Accumulation/Distribution")
plot(ta.wvad, color=color.yellow)

// the same on pine
f_wvad() =>
    (close - open) / (high - low) * volume

plot(f_wvad())
```
