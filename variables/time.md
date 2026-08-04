---
title: "time"
kind: variable
source: https://www.tradingview.com/pine-script-reference/v6/#var_time
---

# time

**Category:** Variable

**Type:** `series int`

## Description

Current bar time in UNIX format. It is the number of milliseconds that have elapsed since 00:00:00 UTC, 1 January 1970.

## Remarks

Note that this variable returns the timestamp based on the time of the bar's open. Because of that, for overnight sessions (e.g. EURUSD, where Monday session starts on Sunday, 17:00) this variable can return time before the specified date of the trading day. For example, on EURUSD, `dayofmonth(time)` can be lower by 1 than the date of the trading day, because the bar for the current day actually opens one day prior.

## See also

- [time()](../functions/time.md)
- [time_close](./time_close.md)
- [timenow](./timenow.md)
- [year](./year.md)
- [month](./month.md)
- [weekofyear](./weekofyear.md)
- [dayofmonth](./dayofmonth.md)
- [dayofweek](./dayofweek.md)
- [hour](./hour.md)
- [minute](./minute.md)
- [second](./second.md)
