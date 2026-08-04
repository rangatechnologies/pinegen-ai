---
title: "footprint.rows"
kind: function
namespace: footprint
source: https://www.tradingview.com/pine-script-reference/v6/#fun_footprint.rows
---

# footprint.rows

**Category:** Function

## Syntax

```pinescript
footprint.rows(id) → array<volume_row>
```

## Description

Creates an array containing all [volume_row](../../types/volume_row.md) IDs from a [footprint](../../types/footprint.md) object. Each [volume_row](../../types/volume_row.md) object referenced in the array contains data for one row in the calculated volume footprint, where the first object represents the lowest row and the last one represents the highest row.

## Arguments

- **`id`** `footprint` — The reference (ID) of the [footprint](../../types/footprint.md) object to analyze.

## Returns

The ID of an array containing a [volume_row](../../types/volume_row.md) ID for each row in the footprint.

**Return type(s):** `array<volume_row>`
