---
title: "-"
kind: operator
source: https://www.tradingview.com/pine-script-reference/v6/#op_-
---

# -

**Category:** Operator

## Syntax

_2 overloaded forms:_

```pinescript
expr1 - expr2
```

```pinescript
- expr
```

## Description

Subtraction or unary minus. Applicable to numerical expressions.

## Returns

Returns integer or float value, or series of values:

Binary `-` returns expr1 minus expr2.

Unary `-` returns the negation of expr.

## Remarks

You may use arithmetic operators with numbers as well as with series variables. In case of usage with series the operators are applied elementwise.
