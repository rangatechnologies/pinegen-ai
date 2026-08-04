---
title: "barstate.isrealtime"
kind: variable
namespace: barstate
source: https://www.tradingview.com/pine-script-reference/v6/#var_barstate.isrealtime
---

# barstate.isrealtime

**Category:** Variable

**Type:** `series bool`

## Description

Returns true if current bar is a real-time bar, false otherwise.

## Remarks

Pine Script® code that uses this variable could calculate differently on history and real-time data.

Please note that using this variable/function can cause [indicator repainting](https://www.tradingview.com/pine-script-docs/concepts/repainting/).

## See also

- [barstate.isfirst](./isfirst.md)
- [barstate.islast](./islast.md)
- [barstate.ishistory](./ishistory.md)
- [barstate.isnew](./isnew.md)
- [barstate.isconfirmed](./isconfirmed.md)
- [barstate.islastconfirmedhistory](./islastconfirmedhistory.md)
