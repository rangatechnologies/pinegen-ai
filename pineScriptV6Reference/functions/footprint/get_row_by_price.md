---
title: "footprint.get_row_by_price"
kind: function
namespace: footprint
source: https://www.tradingview.com/pine-script-reference/v6/#fun_footprint.get_row_by_price
---

# footprint.get_row_by_price

**Category:** Function

## Syntax

```pinescript
footprint.get_row_by_price(id, price) → volume_row
```

## Description

Analyzes the volume footprint represented by a [footprint](../../types/footprint.md) object to find the row whose price range includes the specified price level. If the price belongs to one of the rows, the function returns the ID of the [volume_row](../../types/volume_row.md) object that contains the data for that row. Otherwise, it returns [na](../../variables/na.md).

## Arguments

- **`id`** `footprint` — The reference (ID) of the [footprint](../../types/footprint.md) object to analyze.
- **`price`** `series int/float` — The price value for which to find the corresponding footprint row.

## Returns

The ID of a [volume_row](../../types/volume_row.md) object representing the footprint row that contains the specified price, or [na](../../variables/na.md) if the price is outside the footprint's price range.

**Return type(s):** `volume_row`
