---
title: "=>"
kind: operator
source: https://www.tradingview.com/pine-script-reference/v6/#op_=>
---

# =>

**Category:** Operator

## Syntax

```pinescript
<identifier>([<parameter_name>[=<default_value>]], ...) =>
    <local_block>
    <function_result>
```

## Description

The '=>' operator is used in user-defined function declarations and in [switch](../keywords/switch.md) statements.

The function declaration syntax is:

## Remarks

You can learn more about user-defined functions in the User Manual's pages on [Declaring functions](https://www.tradingview.com/pine-script-docs/language/user-defined-functions/) and [Libraries](https://www.tradingview.com/pine-script-docs/concepts/libraries/).

## Detailed Description

A <local_block> is zero or more Pine Script® statements.

The <function_result> is a variable, an expression, or a tuple.

```pinescript
//@version=6
indicator("=>")
// single-line function
f1(x, y) => x + y
// multi-line function
f2(x, y) =>
	sum = x + y
	sumChange = ta.change(sum, 10)
	// Function automatically returns the last expression used in it
plot(f1(30, 8) + f2(1, 3))
```
