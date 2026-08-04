---
title: "ta.mom"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.mom
---

# ta.mom

**Category:** Function

## Syntax

```pinescript
ta.mom(source, length) → series float
```

## Description

Momentum of `source` price and `source` price `length` bars ago. This is simply a difference: source - source[length].

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `series int` — Offset from the current bar to the previous bar.

## Returns

Momentum of `source` price and `source` price `length` bars ago.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are included in calculations and will produce an `na` result.

## See also

- [ta.change()](./change.md)
