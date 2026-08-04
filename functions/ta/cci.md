---
title: "ta.cci"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.cci
---

# ta.cci

**Category:** Function

## Syntax

```pinescript
ta.cci(source, length) → series float
```

## Description

The CCI (commodity channel index) is calculated as the difference between the typical price of a commodity and its simple moving average, divided by the mean absolute deviation of the typical price. The index is scaled by an inverse factor of 0.015 to provide more readable numbers.

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).

## Returns

Commodity channel index of source for length bars back.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are ignored.
