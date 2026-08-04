---
title: "barstate.islast"
kind: variable
namespace: barstate
source: https://www.tradingview.com/pine-script-reference/v6/#var_barstate.islast
---

# barstate.islast

**Category:** Variable

**Type:** `series bool`

## Description

Returns true if current bar is the last bar in barset, false otherwise. This condition is true for all real-time bars in barset.

## Remarks

Pine Script® code that uses this variable could calculate differently on history and real-time data.

Please note that using this variable/function can cause [indicator repainting](https://www.tradingview.com/pine-script-docs/concepts/repainting/).

## See also

- [barstate.isfirst](./isfirst.md)
- [barstate.ishistory](./ishistory.md)
- [barstate.isrealtime](./isrealtime.md)
- [barstate.isnew](./isnew.md)
- [barstate.isconfirmed](./isconfirmed.md)
- [barstate.islastconfirmedhistory](./islastconfirmedhistory.md)
