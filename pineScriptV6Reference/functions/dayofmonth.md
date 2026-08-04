---
title: "dayofmonth"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_dayofmonth
---

# dayofmonth

**Category:** Function

## Syntax

```pinescript
dayofmonth(time, timezone) → series int
```

## Description

Calculates the day number of the month, in a specified time zone, from a UNIX timestamp.

## Arguments

- **`time`** `series int` — A UNIX timestamp in milliseconds.
- **`timezone`** `series string` — Optional. Specifies the time zone of the returned day number. The value can be a time zone string in UTC/GMT offset notation (e.g., "UTC-5") or IANA time zone database notation (e.g., "America/New_York"). The default is [syminfo.timezone](../variables/syminfo/timezone.md).

## Returns

The calculated day of the month, expressed in the specified time zone.

**Return type(s):** `series int`

## Remarks

A [UNIX timestamp](https://www.tradingview.com/pine-script-docs/concepts/time/#unix-timestamps) represents the number of milliseconds elapsed since 00:00 UTC on 1970-01-01. The meaning of a UNIX timestamp does not change relative to any time zone.

## See also

- [dayofmonth](../variables/dayofmonth.md)
- [dayofweek()](./dayofweek.md)
- [weekofyear()](./weekofyear.md)
- [time()](./time.md)
- [year()](./year.md)
- [month()](./month.md)
- [hour()](./hour.md)
- [minute()](./minute.md)
- [second()](./second.md)
