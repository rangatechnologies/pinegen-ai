---
title: "footprint.delta"
kind: function
namespace: footprint
source: https://www.tradingview.com/pine-script-reference/v6/#fun_footprint.delta
---

# footprint.delta

**Category:** Function

## Syntax

```pinescript
footprint.delta(id) → series float
```

## Description

Calculates the overall volume delta for the volume footprint represented by a [footprint](../../types/footprint.md) object. The value represents the difference between the footprint's total "buy" volume and "sell" volume. A positive value indicates that the total "buy" volume in the footprint exceeds the total "sell" volume, and a negative value indicates the opposite.


## Arguments

- **`id`** `footprint` — The reference (ID) of the [footprint](../../types/footprint.md) object to analyze.

## Returns

The overall volume delta for the footprint.

**Return type(s):** `series float`
