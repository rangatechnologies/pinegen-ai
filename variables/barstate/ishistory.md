---
title: "barstate.ishistory"
kind: variable
namespace: barstate
source: https://www.tradingview.com/pine-script-reference/v6/#var_barstate.ishistory
---

# barstate.ishistory

**Category:** Variable

**Type:** `series bool`

## Description

Returns true if current bar is a historical bar, false otherwise.

## Remarks

Pine Script® code that uses this variable could calculate differently on history and real-time data.

Please note that using this variable/function can cause [indicator repainting](https://www.tradingview.com/pine-script-docs/concepts/repainting/).

## See also

- [barstate.isfirst](./isfirst.md)
- [barstate.islast](./islast.md)
- [barstate.isrealtime](./isrealtime.md)
- [barstate.isnew](./isnew.md)
- [barstate.isconfirmed](./isconfirmed.md)
- [barstate.islastconfirmedhistory](./islastconfirmedhistory.md)
