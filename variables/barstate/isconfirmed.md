---
title: "barstate.isconfirmed"
kind: variable
namespace: barstate
source: https://www.tradingview.com/pine-script-reference/v6/#var_barstate.isconfirmed
---

# barstate.isconfirmed

**Category:** Variable

**Type:** `series bool`

## Description

Returns true if the script is calculating the last (closing) update of the current bar. The next script calculation will be on the new bar data.

## Remarks

Pine Script® code that uses this variable could calculate differently on history and real-time data.

It is NOT recommended to use [barstate.isconfirmed](./isconfirmed.md) in [request.security()](../../functions/request/security.md) expression. Its value requested from [request.security()](../../functions/request/security.md) is unpredictable.

## See also

- [barstate.isfirst](./isfirst.md)
- [barstate.islast](./islast.md)
- [barstate.ishistory](./ishistory.md)
- [barstate.isrealtime](./isrealtime.md)
- [barstate.isnew](./isnew.md)
- [barstate.islastconfirmedhistory](./islastconfirmedhistory.md)
