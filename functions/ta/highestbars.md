---
title: "ta.highestbars"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.highestbars
---

# ta.highestbars

**Category:** Function

## Syntax

```pinescript
ta.highestbars(source, length) → series int
```

## Description

Highest value offset for a given number of bars back.

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).

## Returns

Offset to the highest bar.

**Return type(s):** `series int`

## Remarks

Two args version: `source` is a series and `length` is the number of bars back.

One arg version: `length` is the number of bars back. Algorithm uses high as a `source` series.

`na` values in the `source` series are ignored.

## See also

- [ta.lowest()](./lowest.md)
- [ta.highest()](./highest.md)
- [ta.lowestbars()](./lowestbars.md)
- [ta.barssince()](./barssince.md)
- [ta.valuewhen()](./valuewhen.md)
