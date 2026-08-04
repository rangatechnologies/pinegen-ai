---
title: "ta.barssince"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.barssince
---

# ta.barssince

**Category:** Function

## Syntax

```pinescript
ta.barssince(condition) → series int
```

## Description

Counts the number of bars since the last time the condition was true.

## Arguments

- **`condition`** `series bool` — The condition to check for.

## Returns

Number of bars since condition was true.

**Return type(s):** `series int`

## Remarks

If the condition has never been met prior to the current bar, the function returns na.

Please note that using this variable/function can cause [indicator repainting](https://www.tradingview.com/pine-script-docs/concepts/repainting/).

## Examples

```pinescript
//@version=6
indicator("ta.barssince")
// get number of bars since last color.green bar
plot(ta.barssince(close >= open))
```

## See also

- [ta.lowestbars()](./lowestbars.md)
- [ta.highestbars()](./highestbars.md)
- [ta.valuewhen()](./valuewhen.md)
- [ta.highest()](./highest.md)
- [ta.lowest()](./lowest.md)
