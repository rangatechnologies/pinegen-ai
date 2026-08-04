---
title: "weekofyear"
kind: variable
source: https://www.tradingview.com/pine-script-reference/v6/#var_weekofyear
---

# weekofyear

**Category:** Variable

**Type:** `series int`

## Description

The week number of the year, in the exchange time zone, calculated from the bar's opening UNIX timestamp.

## Remarks

This variable always references the week number corresponding to the bar's opening time. Consequently, for symbols with overnight sessions (e.g., "EURUSD", where the "Monday" session starts on Sunday at 17:00 in exchange time), the value may represent a previous calendar week rather than the week of the session's primary trading day.

## See also

- [weekofyear()](../functions/weekofyear.md)
- [dayofmonth](./dayofmonth.md)
- [dayofweek](./dayofweek.md)
- [time](./time.md)
- [year](./year.md)
- [month](./month.md)
- [hour](./hour.md)
- [minute](./minute.md)
- [second](./second.md)
