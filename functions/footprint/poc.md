---
title: "footprint.poc"
kind: function
namespace: footprint
source: https://www.tradingview.com/pine-script-reference/v6/#fun_footprint.poc
---

# footprint.poc

**Category:** Function

## Syntax

```pinescript
footprint.poc(id) → volume_row
```

## Description

Finds the Point of Control (POC) row for the volume footprint represented by a [footprint](../../types/footprint.md) object, then returns the ID of a [volume_row](../../types/volume_row.md) object containing the data for that row.

## Arguments

- **`id`** `footprint` — The reference (ID) of the [footprint](../../types/footprint.md) object to analyze.

## Returns

The ID of a [volume_row](../../types/volume_row.md) object representing the footprint's POC row.

**Return type(s):** `volume_row`
