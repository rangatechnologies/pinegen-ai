---
title: "dayofmonth"
kind: variable
source: https://www.tradingview.com/pine-script-reference/v6/#var_dayofmonth
---

# dayofmonth

**Category:** Variable

**Type:** `series int`

## Description

The day number of the month, in the exchange time zone, calculated from the bar's opening UNIX timestamp.

## Remarks

This variable always references the day number corresponding to the bar's opening time. Consequently, for symbols with overnight sessions (e.g., "EURUSD", where the "Monday" session starts on Sunday at 17:00 in exchange time), the value may represent a day from the previous week rather than the session's primary trading day.

## See also

- [dayofmonth()](../functions/dayofmonth.md)
- [dayofweek](./dayofweek.md)
- [weekofyear](./weekofyear.md)
- [time](./time.md)
- [year](./year.md)
- [month](./month.md)
- [hour](./hour.md)
- [minute](./minute.md)
- [second](./second.md)
