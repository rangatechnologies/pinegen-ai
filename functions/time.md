---
title: "time"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_time
---

# time

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
time(timeframe, session, bars_back, timeframe_bars_back) → series int
```

```pinescript
time(timeframe, session, timezone, bars_back, timeframe_bars_back) → series int
```

## Description

Returns the opening UNIX timestamp for the specified timeframe and session, or [na](../variables/na.md) if the time point is outside the session.

## Arguments

- **`timeframe`** `series string` — The timeframe of the timestamp calculation. If the value is an empty string, the function uses the script's main timeframe.
- **`session`** `series string` — Optional. The [session string](https://www.tradingview.com/pine-script-docs/concepts/sessions/#creating-time-based-sessions) for filtering times. The function returns a timestamp if the time is in the specified session, or [na](../variables/na.md) if the time is outside the session. If the argument is an empty string, the function uses the default, which is the symbol's session.
- **`bars_back`** `series int` (optional) — Optional. The bar offset on the script's main timeframe. If the value is positive, the function finds the bar that is N bars before the current bar on the main timeframe, then retrieves the timestamp of the corresponding bar on the timeframe specified by the `timeframe` argument. If the value is a negative number from -1 to -500, the function calculates the expected timestamp of the `timeframe` bar corresponding to N bars after the current bar on the main timeframe. The default is 0.
- **`timeframe_bars_back`** `series int` (optional) — Optional. The additional bar offset on the timeframe specified by the `timeframe` argument. If the value is positive, the function retrieves the timestamp of the bar that is N `timeframe` bars before the one corresponding to the `bars_back` offset. If the value is a negative number from -1 to -500, the function calculates the expected timestamp of the `timeframe` bar that is N `timeframe` bars after the one corresponding to the `bars_back` offset. The default is 0.

## Returns

The opening UNIX timestamp.

**Return type(s):** `series int`

## Remarks

UNIX time is a standardized date and time representation that measures the number of non-leap seconds elapsed since January 1, 1970 at 00:00:00 UTC. Pine Script expresses UNIX time values in milliseconds. See the [UNIX timestamps](https://www.tradingview.com/pine-script-docs/concepts/time/#unix-timestamps) section of the User Manual's [Time](https://www.tradingview.com/pine-script-docs/concepts/time/#time) page to learn more.

## Detailed Description



```pinescript
//@version=6
indicator("Time", overlay=true)
// Try this on chart AAPL,1
timeinrange(res, sess) => not na(time(res, sess, "America/New_York")) ? 1 : 0
plot(timeinrange("1", "1300-1400"), color=color.red)

// This plots 1.0 at every start of 10 minute bar on a 1 minute chart:
newbar(res) => ta.change(time(res)) == 0 ? 0 : 1
plot(newbar("10"))
```

---

While setting up a session you can specify not just the hours and minutes but also the days of the week that will be included in that session.

If the days aren't specified, the session is considered to have been set from Sunday (1) to Saturday (7), i.e. "1100-2000" is the same as "1100-1200:1234567".



You can change that by specifying the days. For example, on a symbol that is traded seven days a week with the 24-hour trading session the following script will not color Saturdays and Sundays:

```pinescript
//@version=6
indicator("Time", overlay=true)
t1 = time(timeframe.period, "0000-0000:23456")
bgcolor(not na(t1) ? color.new(color.blue, 90) : na)
```

---

One `session` argument can include several different sessions, separated by commas. For example, the following script will highlight the bars from 10:00 to 11:00 and from 14:00 to 15:00 (workdays only):

```pinescript
//@version=6
indicator("Time", overlay=true)
t1 = time(timeframe.period, "1000-1100,1400-1500:23456")
bgcolor(not na(t1) ? color.new(color.blue, 90) : na)
```

## See also

- [time](../variables/time.md)
