---
title: "time_close"
kind: variable
source: https://www.tradingview.com/pine-script-reference/v6/#var_time_close
---

# time_close

**Category:** Variable

**Type:** `series int`

## Description

The time of the current bar's close in UNIX format. It represents the number of milliseconds elapsed since 00:00:00 UTC, 1 January 1970. On tick charts and price-based charts such as Renko, line break, Kagi, point & figure, and range, this variable's series holds an [na](./na.md) timestamp for the latest realtime bar (because the future closing time is unpredictable), but valid timestamps for all previous bars.

## See also

- [time](./time.md)
- [timenow](./timenow.md)
- [year](./year.md)
- [month](./month.md)
- [weekofyear](./weekofyear.md)
- [dayofmonth](./dayofmonth.md)
- [dayofweek](./dayofweek.md)
- [hour](./hour.md)
- [minute](./minute.md)
- [second](./second.md)
