---
title: "ta.dev"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.dev
---

# ta.dev

**Category:** Function

## Syntax

```pinescript
ta.dev(source, length) → series float
```

## Description

Measure of difference between the series and it's [ta.sma()](./sma.md)

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).

## Returns

Deviation of `source` for `length` bars back.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are ignored.

## Examples

```pinescript
//@version=6
indicator("ta.dev")
plot(ta.dev(close, 10))

// the same on pine
pine_dev(source, length) =>
    mean = ta.sma(source, length)
    sum = 0.0
    for i = 0 to length - 1
        val = source[i]
        sum := sum + math.abs(val - mean)
    dev = sum/length
plot(pine_dev(close, 10))
```

## See also

- [ta.variance()](./variance.md)
- [ta.stdev()](./stdev.md)
