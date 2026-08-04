---
title: "array.new_linefill"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.new_linefill
---

# array.new_linefill

**Category:** Function

## Syntax

```pinescript
array.new_linefill(size, initial_value) → array<linefill>
```

## Description

The function creates a new array object of linefill type elements.

## Arguments

- **`size`** `series int` (optional) — Initial size of an array.
- **`initial_value`** `series linefill` (optional) — Initial value of all array elements.

## Returns

The ID of an array object which may be used in other array.*() functions.

**Return type(s):** `array<linefill>`

## Remarks

An array index starts from 0.
