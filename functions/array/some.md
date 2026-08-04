---
title: "array.some"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.some
---

# array.some

**Category:** Function

## Syntax

```pinescript
array.some(id) → series bool
```

## Description

Returns [true](../../constants/true.md) if at least one element of the `id` array is [true](../../constants/true.md), [false](../../constants/false.md) otherwise.

## Arguments

- **`id`** `array<bool>` — An array object.

**Return type(s):** `series bool`

## Remarks

This function also works with arrays of [int](../../types/int.md) and [float](../../types/float.md) types, in which case zero values are considered [false](../../constants/false.md), and all others [true](../../constants/true.md).

## See also

- [array.every()](./every.md)
- [array.get()](./get.md)
