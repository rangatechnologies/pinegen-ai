---
title: "dayofweek"
kind: variable
source: https://www.tradingview.com/pine-script-reference/v6/#var_dayofweek
---

# dayofweek

**Category:** Variable

**Type:** `series int`

## Description

The day number of the week, in the exchange time zone, calculated from the bar's opening UNIX timestamp.

## Remarks

This variable always references the day number corresponding to the bar's opening time. Consequently, for symbols with overnight sessions (e.g., "EURUSD", where the "Monday" session starts on Sunday at 17:00 in exchange time), the value may represent a day from the previous week rather than the session's primary trading day.

You can use [dayofweek.sunday](../constants/dayofweek/sunday.md), [dayofweek.monday](../constants/dayofweek/monday.md), [dayofweek.tuesday](../constants/dayofweek/tuesday.md), [dayofweek.wednesday](../constants/dayofweek/wednesday.md), [dayofweek.thursday](../constants/dayofweek/thursday.md), [dayofweek.friday](../constants/dayofweek/friday.md) and [dayofweek.saturday](../constants/dayofweek/saturday.md) variables for comparisons.

## See also

- [dayofweek()](../functions/dayofweek.md)
- [time](./time.md)
- [year](./year.md)
- [month](./month.md)
- [weekofyear](./weekofyear.md)
- [dayofmonth](./dayofmonth.md)
- [hour](./hour.md)
- [minute](./minute.md)
- [second](./second.md)
