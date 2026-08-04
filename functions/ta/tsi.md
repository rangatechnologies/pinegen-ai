---
title: "ta.tsi"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.tsi
---

# ta.tsi

**Category:** Function

## Syntax

```pinescript
ta.tsi(source, short_length, long_length) → series float
```

## Description

True strength index. It uses moving averages of the underlying momentum of a financial instrument.

## Arguments

- **`source`** `series int/float` — Source series.
- **`short_length`** `simple int` — Short length.
- **`long_length`** `simple int` — Long length.

## Returns

True strength index. A value in range [-1, 1].

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are ignored; the function calculates on the `length` quantity of non-`na` values.
