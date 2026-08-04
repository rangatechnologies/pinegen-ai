---
title: "ta.cmo"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.cmo
---

# ta.cmo

**Category:** Function

## Syntax

```pinescript
ta.cmo(series, length) → series float
```

## Description

Chande Momentum Oscillator. Calculates the difference between the sum of recent gains and the sum of recent losses and then divides the result by the sum of all price movement over the same period.

## Arguments

- **`series`** `series int/float` — Series of values to process.
- **`length`** `series int` — Number of bars (length).

## Returns

Chande Momentum Oscillator.

**Return type(s):** `series float`

## Remarks

`na` values in the `source` series are ignored.

## Examples

```pinescript
//@version=6
indicator("ta.cmo")
plot(ta.cmo(close, 5), color=color.yellow)

// the same on pine
f_cmo(src, length) =>
    float mom = ta.change(src)
    float sm1 = math.sum((mom >= 0) ? mom : 0.0, length)
    float sm2 = math.sum((mom >= 0) ? 0.0 : -mom, length)
    100 * (sm1 - sm2) / (sm1 + sm2)

plot(f_cmo(close, 5))
```

## See also

- [ta.rsi()](./rsi.md)
- [ta.stoch()](./stoch.md)
- [math.sum()](../math/sum.md)
