---
title: "ta.lowestbars"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.lowestbars
---

# ta.lowestbars

**Category:** Function

## Syntax

```pinescript
ta.lowestbars(source, length) → series int
```

## Description

Lowest value offset for a given number of bars back.

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars back.

## Returns

Offset to the lowest bar.

**Return type(s):** `series int`

## Remarks

Two args version: `source` is a series and `length` is the number of bars back.

One arg version: `length` is the number of bars back. Algorithm uses low as a `source` series.

`na` values in the `source` series are ignored.

## See also

- [ta.lowest()](./lowest.md)
- [ta.highest()](./highest.md)
- [ta.highestbars()](./highestbars.md)
- [ta.barssince()](./barssince.md)
- [ta.valuewhen()](./valuewhen.md)
