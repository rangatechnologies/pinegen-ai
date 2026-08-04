---
title: "month"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_month
---

# month

**Category:** Function

## Syntax

```pinescript
month(time, timezone) → series int
```

## Arguments

- **`time`** `series int` — UNIX time in milliseconds.
- **`timezone`** `series string` — Allows adjusting the returned value to a time zone specified in either UTC/GMT notation (e.g., "UTC-5", "GMT+0530") or as an IANA time zone database name (e.g., "America/New_York"). Optional. The default is [syminfo.timezone](../variables/syminfo/timezone.md).

## Returns

Month (in exchange timezone) for provided UNIX time.

**Return type(s):** `series int`

## Remarks

UNIX time is the number of milliseconds that have elapsed since 00:00:00 UTC, 1 January 1970.

Note that this function returns the month based on the time of the bar's open. For overnight sessions (e.g. EURUSD, where Monday session starts on Sunday, 17:00 UTC-4) this value can be lower by 1 than the month of the trading day.

## See also

- [month](../variables/month.md)
- [time()](./time.md)
- [year()](./year.md)
- [dayofmonth()](./dayofmonth.md)
- [dayofweek()](./dayofweek.md)
- [hour()](./hour.md)
- [minute()](./minute.md)
- [second()](./second.md)
