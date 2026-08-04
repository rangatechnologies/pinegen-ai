---
title: "math.avg"
kind: function
namespace: math
source: https://www.tradingview.com/pine-script-reference/v6/#fun_math.avg
---

# math.avg

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
math.avg(number0, number1, ...) → simple float
```

```pinescript
math.avg(number0, number1, ...) → series float
```

## Description

Calculates average of all given series (elementwise).

## Arguments

- **`number0, number1, ...`** `simple int/float` — A sequence of numbers to use in the calculation.

## Returns

Average.

**Return type(s):** `simple float`

## See also

- [math.sum()](./sum.md)
- [ta.cum()](../ta/cum.md)
- [ta.sma()](../ta/sma.md)
