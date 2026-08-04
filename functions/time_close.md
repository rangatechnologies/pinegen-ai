---
title: "time_close"
kind: function
source: https://www.tradingview.com/pine-script-reference/v6/#fun_time_close
---

# time_close

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
time_close(timeframe, session, bars_back, timeframe_bars_back) → series int
```

```pinescript
time_close(timeframe, session, timezone, bars_back, timeframe_bars_back) → series int
```

## Description

Returns the closing UNIX timestamp for the specified timeframe and session, or [na](../variables/na.md) if the time point is outside the session. On tick charts and price-based charts such as Renko, line break, Kagi, point & figure, and range, the function returns [na](../variables/na.md) on the latest realtime bar because the future closing time is unpredictable. However, it returns a valid timestamp for any previous bar.

## Arguments

- **`timeframe`** `series string` — The timeframe of the timestamp calculation. If the value is an empty string, the function uses the script's main timeframe.
- **`session`** `series string` — Optional. The [session string](https://www.tradingview.com/pine-script-docs/concepts/sessions/#creating-time-based-sessions) for filtering times. The function returns a timestamp if the time is in the specified session, or [na](../variables/na.md) if the time is outside the session. If the argument is an empty string, the function uses the default, which is the symbol's session.
- **`bars_back`** `series int` (optional) — Optional. The bar offset on the script's main timeframe. If the value is positive, the function finds the bar that is N bars before the current bar on the main timeframe, then retrieves the timestamp of the corresponding bar on the timeframe specified by the `timeframe` argument. If the value is a negative number from -1 to -500, the function calculates the expected timestamp of the `timeframe` bar corresponding to N bars after the current bar on the main timeframe. The default is 0.
- **`timeframe_bars_back`** `series int` (optional) — Optional. The additional bar offset on the timeframe specified by the `timeframe` argument. If the value is positive, the function retrieves the timestamp of the bar that is N `timeframe` bars before the one corresponding to the `bars_back` offset. If the value is a negative number from -1 to -500, the function calculates the expected timestamp of the `timeframe` bar that is N `timeframe` bars after the one corresponding to the `bars_back` offset. The default is 0.

## Returns

The closing UNIX timestamp.

**Return type(s):** `series int`

## Remarks

UNIX time is a standardized date and time representation that measures the number of non-leap seconds elapsed since January 1, 1970 at 00:00:00 UTC. Pine Script expresses UNIX time values in milliseconds. See the [UNIX timestamps](https://www.tradingview.com/pine-script-docs/concepts/time/#unix-timestamps) section of the User Manual's [Time](https://www.tradingview.com/pine-script-docs/concepts/time/#time) page to learn more.

## Detailed Description



```pinescript
//@version=6
indicator("Time", overlay=true)
t1 = time_close(timeframe.period, "1200-1300", "America/New_York")
bgcolor(not na(t1) ? color.new(color.blue, 90) : na)
```

## See also

- [time_close](../variables/time_close.md)
