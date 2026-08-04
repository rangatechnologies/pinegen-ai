---
title: "timestamp"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_timestamp
---

# timestamp

**Category:** Function

## Syntax

_6 overloaded forms:_

```pinescript
timestamp(dateString) → const int
```

```pinescript
timestamp(dateString) → series int
```

```pinescript
timestamp(year, month, day, hour, minute, second) → simple int
```

```pinescript
timestamp(year, month, day, hour, minute, second) → series int
```

```pinescript
timestamp(timezone, year, month, day, hour, minute, second) → simple int
```

```pinescript
timestamp(timezone, year, month, day, hour, minute, second) → series int
```

## Description

Function timestamp returns UNIX time of specified date and time.

## Arguments

- **`dateString`** `const string` — A string containing the date and, optionally, the time and time zone. Its format must comply with either the [IETF RFC 2822](https://tools.ietf.org/html/rfc2822#section-3.3) or [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) standards ("DD MMM YYYY hh:mm:ss ±hhmm" or "YYYY-MM-DDThh:mm:ss±hh:mm", so "20 Feb 2020" or "2020-02-20"). If no time is supplied, "00:00" is used. If no time zone is supplied, GMT+0 will be used. Note that this diverges from the usual behavior of the function where it returns time in the exchange's timezone.

## Returns

UNIX time.

**Return type(s):** `const int`

## Remarks

UNIX time is the number of milliseconds that have elapsed since 00:00:00 UTC, 1 January 1970.

## Examples

```pinescript
//@version=6
indicator("timestamp")
plot(timestamp(2016, 01, 19, 09, 30), linewidth=3, color=color.green)
plot(timestamp(syminfo.timezone, 2016, 01, 19, 09, 30), color=color.blue)
plot(timestamp(2016, 01, 19, 09, 30), color=color.yellow)
plot(timestamp("GMT+6", 2016, 01, 19, 09, 30))
plot(timestamp(2019, 06, 19, 09, 30, 15), color=color.lime)
plot(timestamp("GMT+3", 2019, 06, 19, 09, 30, 15), color=color.fuchsia)
plot(timestamp("Feb 01 2020 22:10:05"))
plot(timestamp("2011-10-10T14:48:00"))
plot(timestamp("04 Dec 1995 00:12:00 GMT+5"))
```

## See also

- [time()](./time.md)
- [time](../variables/time.md)
- [timenow](../variables/timenow.md)
- [syminfo.timezone](../variables/syminfo/timezone.md)
