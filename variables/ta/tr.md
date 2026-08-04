---
title: "ta.tr"
kind: variable
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#var_ta.tr
---

# ta.tr

**Category:** Variable

**Type:** `series float`

## Description

True range, equivalent to `ta.tr(handle_na = false)`. It is calculated as `math.max(high - low, math.abs(high - close[1]), math.abs(low - close[1]))`.

## See also

- [ta.tr()](../../functions/ta/tr.md)
- [ta.atr()](../../functions/ta/atr.md)
