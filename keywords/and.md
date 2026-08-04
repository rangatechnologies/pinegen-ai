---
title: "and"
kind: keyword
source: https://www.tradingview.com/pine-script-reference/v6/#kw_and
---

# and

**Category:** Keyword

## Syntax

```pinescript
expr1 and expr2
```

## Description

Logical AND. Applicable to boolean expressions.

## Returns

Boolean value, or series of boolean values.

## Remarks

If `expr1` evaluates to [false](../constants/false.md), the `and` operator returns [false](../constants/false.md) without evaluating `expr2`.
