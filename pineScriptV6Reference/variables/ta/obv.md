---
title: "ta.obv"
kind: variable
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#var_ta.obv
---

# ta.obv

**Category:** Variable

**Type:** `series float`

## Description

On Balance Volume.

## Examples

```pinescript
//@version=6
indicator("On Balance Volume")
plot(ta.obv, color=color.yellow)

// the same on pine
f_obv() =>
    ta.cum(math.sign(ta.change(close)) * volume)

plot(f_obv())
```
