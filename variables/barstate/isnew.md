---
title: "barstate.isnew"
kind: variable
namespace: barstate
source: https://www.tradingview.com/pine-script-reference/v6/#var_barstate.isnew
---

# barstate.isnew

**Category:** Variable

**Type:** `series bool`

## Description

Returns true if script is currently calculating on new bar, false otherwise. This variable is true when calculating on historical bars or on first update of a newly generated real-time bar.

## Remarks

Pine Script® code that uses this variable could calculate differently on history and real-time data.

Please note that using this variable/function can cause [indicator repainting](https://www.tradingview.com/pine-script-docs/concepts/repainting/).

## See also

- [barstate.isfirst](./isfirst.md)
- [barstate.islast](./islast.md)
- [barstate.ishistory](./ishistory.md)
- [barstate.isrealtime](./isrealtime.md)
- [barstate.isconfirmed](./isconfirmed.md)
- [barstate.islastconfirmedhistory](./islastconfirmedhistory.md)
