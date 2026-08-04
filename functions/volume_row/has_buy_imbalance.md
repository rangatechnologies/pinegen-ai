---
title: "volume_row.has_buy_imbalance"
kind: function
namespace: volume_row
source: https://www.tradingview.com/pine-script-reference/v6/#fun_volume_row.has_buy_imbalance
---

# volume_row.has_buy_imbalance

**Category:** Function

## Syntax

```pinescript
volume_row.has_buy_imbalance(id) → series bool
```

## Description

Checks whether the volume footprint row represented by a [volume_row](../../types/volume_row.md) object has a "buy" imbalance, based on the `imbalance_percent` argument of the [request.footprint()](../request/footprint.md) call that the object depends on. Returns `true` if the row's "buy" volume exceeds the "sell" volume of the row below it in the footprint by the specified percentage, and `false` otherwise.

## Arguments

- **`id`** `volume_row` — The reference (ID) of the [volume_row](../../types/volume_row.md) object to analyze.

## Returns

A value of `true` if the footprint row has a detected buy imbalance, and `false` otherwise.

**Return type(s):** `series bool`
