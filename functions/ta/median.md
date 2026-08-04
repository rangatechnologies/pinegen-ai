---
title: "ta.median"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.median
---

# ta.median

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
ta.median(source, length) → series float
```

```pinescript
ta.median(source, length) → series int
```

## Description

Returns the median of the series.

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).

## Returns

The median of the series.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are ignored; the function calculates on the `length` quantity of non-`na` values.
