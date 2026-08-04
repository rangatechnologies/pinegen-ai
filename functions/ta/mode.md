---
title: "ta.mode"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.mode
---

# ta.mode

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
ta.mode(source, length) → series float
```

```pinescript
ta.mode(source, length) → series int
```

## Description

Returns the [mode](https://en.wikipedia.org/wiki/Mode_(statistics)) of the series. If there are several values with the same frequency, it returns the smallest value.

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).

## Returns

The most frequently occurring value from the `source`. If none exists, returns the smallest value instead.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are ignored; the function calculates on the `length` quantity of non-`na` values.
