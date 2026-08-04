---
title: "+"
kind: operator
source: https://www.tradingview.com/pine-script-reference/v6/#op_+
---

# +

**Category:** Operator

## Syntax

_2 overloaded forms:_

```pinescript
expr1 + expr2
```

```pinescript
+ expr
```

## Description

Addition or unary plus. Applicable to numerical expressions or strings.

## Returns

Binary `+` for strings returns concatenation of expr1 and expr2

For numbers returns integer or float value, or series of values:

Binary `+` returns expr1 plus expr2.

Unary `+` returns expr (does nothing added just for the symmetry with the unary - operator).

## Remarks

You may use arithmetic operators with numbers as well as with series variables. In case of usage with series the operators are applied elementwise.
