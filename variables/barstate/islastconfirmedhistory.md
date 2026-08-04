---
title: "barstate.islastconfirmedhistory"
kind: variable
namespace: barstate
source: https://www.tradingview.com/pine-script-reference/v6/#var_barstate.islastconfirmedhistory
---

# barstate.islastconfirmedhistory

**Category:** Variable

**Type:** `series bool`

## Description

Returns true if script is executing on the dataset's last bar when market is closed, or script is executing on the bar immediately preceding the real-time bar, if market is open. Returns false otherwise.

## Remarks

Pine Script® code that uses this variable could calculate differently on history and real-time data.

Please note that using this variable/function can cause [indicator repainting](https://www.tradingview.com/pine-script-docs/concepts/repainting/).

## See also

- [barstate.isfirst](./isfirst.md)
- [barstate.islast](./islast.md)
- [barstate.ishistory](./ishistory.md)
- [barstate.isrealtime](./isrealtime.md)
- [barstate.isnew](./isnew.md)
