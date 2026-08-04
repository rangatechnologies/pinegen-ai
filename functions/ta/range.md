---
title: "ta.range"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.range
---

# ta.range

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
ta.range(source, length) → series float
```

```pinescript
ta.range(source, length) → series int
```

## Description

Returns the difference between the min and max values in a series.

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).

## Returns

The difference between the min and max values in the series.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are ignored; the function calculates on the `length` quantity of non-`na` values.
