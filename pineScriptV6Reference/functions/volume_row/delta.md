---
title: "volume_row.delta"
kind: function
namespace: volume_row
source: https://www.tradingview.com/pine-script-reference/v6/#fun_volume_row.delta
---

# volume_row.delta

**Category:** Function

## Syntax

```pinescript
volume_row.delta(id) → series float
```

## Description

Calculates the volume delta for the volume footprint row represented by a [volume_row](../../types/volume_row.md) object. The value represents the difference between the row's "buy" volume and "sell" volume. A positive value indicates that the "buy" volume for the row exceeds the "sell" volume, and a negative value indicates the opposite.

## Arguments

- **`id`** `volume_row` — The reference (ID) of the [volume_row](../../types/volume_row.md) object to analyze.

## Returns

The volume delta for the footprint row.

**Return type(s):** `series float`
