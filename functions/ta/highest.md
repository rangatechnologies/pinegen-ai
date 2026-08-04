---
title: "ta.highest"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.highest
---

# ta.highest

**Category:** Function

## Syntax

```pinescript
ta.highest(source, length) → series float
```

## Description

Highest value for a given number of bars back.

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).

## Returns

Highest value in the series.

**Return type(s):** `series float`

## Remarks

Two args version: `source` is a series and `length` is the number of bars back.

One arg version: `length` is the number of bars back. Algorithm uses high as a `source` series.

`na` values in the `source` series are ignored.

## See also

- [ta.lowest()](./lowest.md)
- [ta.lowestbars()](./lowestbars.md)
- [ta.highestbars()](./highestbars.md)
- [ta.valuewhen()](./valuewhen.md)
- [ta.barssince()](./barssince.md)
