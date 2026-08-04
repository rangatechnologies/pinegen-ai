---
title: "!="
kind: operator
source: https://www.tradingview.com/pine-script-reference/v6/#op_!=
---

# !=

**Category:** Operator

## Syntax

```pinescript
expr1 != expr2
```

## Description

Inequality operator. Returns [true](../constants/true.md) if the operands are considered not equal, and [false](../constants/false.md) otherwise. This operator is compatible with all value types, including "int", "float", "bool", "color", and "string". The operator can also compare two line or label IDs.

## Returns

Boolean value, or series of boolean values.

## Remarks

This operator rounds "float" operands to nine fractional digits.
