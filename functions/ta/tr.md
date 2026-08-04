---
title: "ta.tr"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.tr
---

# ta.tr

**Category:** Function

## Syntax

```pinescript
ta.tr(handle_na) → series float
```

## Description

Calculates the current bar's true range. Unlike a bar's actual range (`high - low`), true range accounts for potential gaps by taking the maximum of the current bar's actual range and the absolute distances from the previous bar's [close](../../variables/close.md) to the current bar's [high](../../variables/high.md) and [low](../../variables/low.md). The formula is: `math.max(high - low, math.abs(high - close[1]), math.abs(low - close[1]))`.

## Arguments

- **`handle_na`** `simple bool` — Defines how the function calculates the result when the previous bar's [close](../../variables/close.md) is [na](../../variables/na.md). If [true](../../constants/true.md), the function returns the bar's `high - low` value. If [false](../../constants/false.md), it returns [na](../../variables/na.md).

## Returns

True range. It is math.max(high - low, math.abs(high - close[1]), math.abs(low - close[1])).

**Return type(s):** `series float`

## Remarks

ta.tr(false) is exactly the same as [ta.tr](../../variables/ta/tr.md).

## See also

- [ta.tr](../../variables/ta/tr.md)
- [ta.atr()](./atr.md)
