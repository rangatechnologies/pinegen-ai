---
title: "ta.falling"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.falling
---

# ta.falling

**Category:** Function

## Syntax

```pinescript
ta.falling(source, length) → series bool
```

## Description

Test if the `source` series is now falling for `length` bars long.

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).

## Returns

true if current `source` value is less than any previous `source` value for `length` bars back, false otherwise.

**Return type(s):** `series bool`

## Remarks

`na` values in the `source` series are ignored; the function calculates on the `length` quantity of non-`na` values.

## See also

- [ta.rising()](./rising.md)
