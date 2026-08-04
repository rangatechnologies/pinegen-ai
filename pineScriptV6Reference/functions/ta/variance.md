---
title: "ta.variance"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.variance
---

# ta.variance

**Category:** Function

## Syntax

```pinescript
ta.variance(source, length, biased) → series float
```

## Description

Variance is the expectation of the squared deviation of a series from its mean ([ta.sma()](./sma.md)), and it informally measures how far a set of numbers are spread out from their mean.

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).
- **`biased`** `series bool` (optional) — Determines which estimate should be used. Optional. The default is true.

## Returns

Variance of `source` for `length` bars back.

**Return type(s):** `series float`

## Remarks

If `biased` is true, function will calculate using a biased estimate of the entire population, if false - unbiased estimate of a sample.

`na` values in the `source` series are ignored; the function calculates on the `length` quantity of non-`na` values.

## See also

- [ta.dev()](./dev.md)
- [ta.stdev()](./stdev.md)
