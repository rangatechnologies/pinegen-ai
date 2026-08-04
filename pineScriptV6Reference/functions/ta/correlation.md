---
title: "ta.correlation"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.correlation
---

# ta.correlation

**Category:** Function

## Syntax

```pinescript
ta.correlation(source1, source2, length) → series float
```

## Description

Correlation coefficient. Describes the degree to which two series tend to deviate from their [ta.sma()](./sma.md) values.

## Arguments

- **`source1`** `series int/float` — Source series.
- **`source2`** `series int/float` — Target series.
- **`length`** `series int` — Length (number of bars back).

## Returns

Correlation coefficient.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are ignored; the function calculates on the `length` quantity of non-`na` values.

## See also

- [request.security()](../request/security.md)
