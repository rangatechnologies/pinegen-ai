---
title: "ta.linreg"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.linreg
---

# ta.linreg

**Category:** Function

## Syntax

```pinescript
ta.linreg(source, length, offset) → series float
```

## Description

Linear regression curve. A line that best fits the prices specified over a user-defined time period. It is calculated using the least squares method. The result of this function is calculated using the formula: linreg = intercept + slope * (length - 1 - offset), where intercept and slope are the values calculated with the least squares method on `source` series.

## Arguments

- **`source`** `series int/float` — Source series.
- **`length`** `series int` — Number of bars (length).
- **`offset`** `simple int` — Offset.

## Returns

Linear regression curve.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are included in calculations and will produce an `na` result.
