---
title: ":="
kind: operator
source: https://www.tradingview.com/pine-script-reference/v6/#op_:=
---

# :=

**Category:** Operator

## Syntax

```pinescript
<var_name> := <new_value>
```

## Description

Reassignment operator. It is used to assign a new value to a previously declared variable.

## Examples

```pinescript
//@version=6
indicator("My script")

myVar = 10

if close > open
    // Modifies the existing global scope `myVar` variable by changing its value from 10 to 20.
    myVar := 20
    // Creates a new `myVar` variable local to the `if` condition and unreachable from the global scope.
    // Does not affect the `myVar` declared in global scope.
    myVar = 30

plot(myVar)
```
