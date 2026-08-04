---
title: "*="
kind: operator
source: https://www.tradingview.com/pine-script-reference/v6/#op_*=
---

# *=

**Category:** Operator

## Syntax

```pinescript
expr1 *= expr2
```

## Description

Multiplication assignment. Applicable to numerical expressions.

## Returns

Integer or float value, or series of values.

## Examples

```pinescript
//@version=6
indicator("*=")
// Equals to expr1 = expr1 * expr2.
a = 2
b = 3
a *= b
// Result: a = 6.
plot(a)
```
