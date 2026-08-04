---
title: "or"
kind: keyword
source: https://www.tradingview.com/pine-script-reference/v6/#kw_or
---

# or

**Category:** Keyword

## Syntax

```pinescript
expr1 or expr2
```

## Description

Logical OR. Applicable to boolean expressions.

## Returns

Boolean value, or series of boolean values.

## Remarks

If `expr1` evaluates to [true](../constants/true.md), the `or` operator returns [true](../constants/true.md) without evaluating `expr2`.
