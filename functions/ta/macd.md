---
title: "ta.macd"
kind: function
namespace: ta
source: https://www.tradingview.com/pine-script-reference/v6/#fun_ta.macd
---

# ta.macd

**Category:** Function

## Syntax

```pinescript
ta.macd(source, fastlen, slowlen, siglen) → [series float, series float, series float]
```

## Description

MACD (moving average convergence/divergence). It is supposed to reveal changes in the strength, direction, momentum, and duration of a trend in a stock's price.

## Arguments

- **`source`** `series int/float` — Series of values to process.
- **`fastlen`** `simple int` — Fast Length parameter.
- **`slowlen`** `simple int` — Slow Length parameter.
- **`siglen`** `simple int` — Signal Length parameter.

## Returns

[Tuple](https://www.tradingview.com/pine-script-docs/language/type-system/#tuples) of three MACD series: MACD line, signal line and histogram line.

**Return type(s):** `[series float, series float, series float]`

## Remarks

`na` values in the `source` series are ignored; the function calculates on the `length` quantity of non-`na` values.

## Detailed Description



```pinescript
//@version=6
indicator("MACD")
[macdLine, signalLine, histLine] = ta.macd(close, 12, 26, 9)
plot(macdLine, color=color.blue)
plot(signalLine, color=color.orange)
plot(histLine, color=color.red, style=plot.style_histogram)
```

---

If you need only one value, use placeholders '_' like this:

```pinescript
//@version=6
indicator("MACD")
[_, signalLine, _] = ta.macd(close, 12, 26, 9)
plot(signalLine, color=color.orange)
```

## See also

- [ta.sma()](./sma.md)
- [ta.ema()](./ema.md)
