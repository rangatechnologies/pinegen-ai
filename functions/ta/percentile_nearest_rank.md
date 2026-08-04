---
title: "ta.percentile_nearest_rank"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.percentile_nearest_rank
---

# ta.percentile_nearest_rank

**Category:** Function

## Syntax

```pinescript
ta.percentile_nearest_rank(source, length, percentage) → series float
```

## Description

Calculates percentile using method of Nearest Rank.

## Arguments

- **`source`** `series int/float` — Series of values to process (source).
- **`length`** `series int` — Number of bars back (length).
- **`percentage`** `simple int/float` — Percentage, a number from range 0..100.

## Returns

P-th percentile of `source` series for `length` bars back.

**Return type(s):** `series float`

## Remarks

Using the Nearest Rank method on lengths less than 100 bars back can result in the same number being used for more than one percentile.

A percentile calculated using the Nearest Rank method will always be a member of the input data set.

The 100th percentile is defined to be the largest value in the input data set.

`na` values in the `source` series are ignored.

## See also

- [ta.percentile_linear_interpolation()](./percentile_linear_interpolation.md)
- http://en.wikipedia.org/wiki/Percentile#The_Nearest_Rank_method
