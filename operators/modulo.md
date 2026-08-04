---
title: "%"
kind: operator
source: https://www.tradingview.com/pine-script-reference/v6/#op_%
---

# %

**Category:** Operator

## Syntax

```pinescript
expr1 % expr2
```

## Description

Modulo (integer remainder). Applicable to numerical expressions.

## Returns

Integer or float value, or series of values.

## Remarks

In Pine Script®, when the integer remainder is calculated, the quotient is truncated, i.e. rounded towards the lowest absolute value. The resulting value will have the same sign as the dividend.

Example: `-1 % 9 = -1 - 9 * int(-1/9) = -1 - 9 * int(-0.111) = -1 - 9 * 0 = -1.`
