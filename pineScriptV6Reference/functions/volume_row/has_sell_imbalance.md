---
title: "volume_row.has_sell_imbalance"
kind: function
namespace: volume_row
source: https://www.tradingview.com/pine-script-reference/v6/#fun_volume_row.has_sell_imbalance
---

# volume_row.has_sell_imbalance

**Category:** Function

## Syntax

```pinescript
volume_row.has_sell_imbalance(id) → series bool
```

## Description

Checks whether the volume footprint row represented by a [volume_row](../../types/volume_row.md) object has a sell imbalance, based on the `imbalance_percent` argument of the [request.footprint()](../request/footprint.md) call that the object depends on. Returns `true` if the row's "sell" volume exceeds the "buy" volume of the row above it in the footprint by the specified percentage, and `false` otherwise.

## Arguments

- **`id`** `volume_row` — The reference (ID) of the [volume_row](../../types/volume_row.md) object to analyze.

## Returns

A value of `true` if the footprint row has a detected sell imbalance, and `false` otherwise.

**Return type(s):** `series bool`
