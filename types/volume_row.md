---
title: "volume_row"
kind: type
source: https://www.tradingview.com/pine-script-reference/v6/#type_volume_row
---

# volume_row

**Category:** Type

## Description

A keyword that explicitly declares the type of a variable or parameter as `volume_row`. All `footprint.*()` functions that retrieve row data from a [footprint](./footprint.md) object return an ID of the `volume_row` type. Scripts can use IDs of this type with the built-in `volume_row.*()` functions to retrieve information about a requested footprint row, including the row's price levels, categorized volume, volume delta, and imbalances.

## See also

- [footprint](./footprint.md)
- [volume_row.up_price()](../functions/volume_row/up_price.md)
- [volume_row.down_price()](../functions/volume_row/down_price.md)
- [volume_row.total_volume()](../functions/volume_row/total_volume.md)
- [volume_row.buy_volume()](../functions/volume_row/buy_volume.md)
- [volume_row.sell_volume()](../functions/volume_row/sell_volume.md)
- [volume_row.delta()](../functions/volume_row/delta.md)
- [volume_row.has_buy_imbalance()](../functions/volume_row/has_buy_imbalance.md)
- [volume_row.has_sell_imbalance()](../functions/volume_row/has_sell_imbalance.md)
