---
title: "ta.rising"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.rising
---

# ta.rising

**Category:** Function

## Syntax

```pinescript
ta.rising(source, length) → series bool
```

## Description

Test if the `source` series is now rising for `length` bars long.

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).

## Returns

true if current `source` is greater than any previous `source` for `length` bars back, false otherwise.

**Return type(s):** `series bool`

## Remarks

`na` values in the `source` series are ignored.

## See also

- [ta.falling()](./falling.md)
