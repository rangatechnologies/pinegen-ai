---
title: "array.every"
kind: function
namespace: array
source: https://www.tradingview.com/pine-script-reference/v6/#fun_array.every
---

# array.every

**Category:** Function

## Syntax

```pinescript
array.every(id) → series bool
```

## Description

Returns [true](../../constants/true.md) if all elements of the `id` array are [true](../../constants/true.md), [false](../../constants/false.md) otherwise.

## Arguments

- **`id`** `array<bool>` — An array object.

**Return type(s):** `series bool`

## Remarks

This function also works with arrays of [int](../../types/int.md) and [float](../../types/float.md) types, in which case zero values are considered [false](../../constants/false.md), and all others [true](../../constants/true.md).

## See also

- [array.some()](./some.md)
- [array.get()](./get.md)
