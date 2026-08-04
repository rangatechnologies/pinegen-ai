---
title: "hour"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_hour
---

# hour

**Category:** Function

## Syntax

```pinescript
hour(time, timezone) → series int
```

## Arguments

- **`time`** `series int` — UNIX time in milliseconds.
- **`timezone`** `series string` — Allows adjusting the returned value to a time zone specified in either UTC/GMT notation (e.g., "UTC-5", "GMT+0530") or as an IANA time zone database name (e.g., "America/New_York"). Optional. The default is [syminfo.timezone](../variables/syminfo/timezone.md).

## Returns

Hour (in exchange timezone) for provided UNIX time.

**Return type(s):** `series int`

## Remarks

UNIX time is the number of milliseconds that have elapsed since 00:00:00 UTC, 1 January 1970.

## See also

- [hour](../variables/hour.md)
- [time()](./time.md)
- [year()](./year.md)
- [month()](./month.md)
- [dayofmonth()](./dayofmonth.md)
- [dayofweek()](./dayofweek.md)
- [minute()](./minute.md)
- [second()](./second.md)
