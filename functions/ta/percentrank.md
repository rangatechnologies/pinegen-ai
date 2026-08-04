---
title: "ta.percentrank"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.percentrank
---

# ta.percentrank

**Category:** Function

## Syntax

```pinescript
ta.percentrank(source, length) → series float
```

## Description

Percent rank is the percents of how many previous values was less than or equal to the current value of given series.

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).

## Returns

Percent rank of `source` for `length` bars back.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are included in calculations and will produce an `na` result.
