---
title: "ta.lowest"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.lowest
---

# ta.lowest

**Category:** Function

## Syntax

```pinescript
ta.lowest(source, length) → series float
```

## Description

Lowest value for a given number of bars back.

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).

## Returns

Lowest value in the series.

**Return type(s):** `series float`

## Remarks

Two args version: `source` is a series and `length` is the number of bars back.

One arg version: `length` is the number of bars back. Algorithm uses low as a `source` series.

`na` values in the `source` series are ignored.

## See also

- [ta.highest()](./highest.md)
- [ta.lowestbars()](./lowestbars.md)
- [ta.highestbars()](./highestbars.md)
- [ta.valuewhen()](./valuewhen.md)
- [ta.barssince()](./barssince.md)
