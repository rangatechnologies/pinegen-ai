---
title: "ta.roc"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.roc
---

# ta.roc

**Category:** Function

## Syntax

```pinescript
ta.roc(source, length) → series float
```

## Description

Calculates the percentage of change (rate of change) between the current value of `source` and its value `length` bars ago.

It is calculated by the formula: 100 * change(src, length) / src[length].

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).

## Returns

The rate of change of `source` for `length` bars back.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are included in calculations and will produce an `na` result.
