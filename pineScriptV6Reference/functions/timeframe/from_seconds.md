---
title: "timeframe.from_seconds"
kind: function
namespace: timeframe
source: https://www.tradingview.com/pine-script-reference/v6/#fun_timeframe.from_seconds
---

# timeframe.from_seconds

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
timeframe.from_seconds(seconds) → simple string
```

```pinescript
timeframe.from_seconds(seconds) → series string
```

## Description

Converts a number of seconds into a valid timeframe string.

## Arguments

- **`seconds`** `simple int` — The number of seconds in the timeframe.

## Returns

A timeframe string compliant with [timeframe string specifications](https://www.tradingview.com/pine-script-docs/concepts/timeframes/#timeframe-string-specifications).

**Return type(s):** `simple string`

## Remarks

If no valid timeframe exists for the quantity of seconds supplied, the next higher valid timeframe will be returned. Accordingly, one second or less will return "1S", 2-5 seconds will return "5S", and 604,799 seconds (one second less than 7 days) will return "7D".

If the seconds exactly represent two or more valid timeframes, the one with the larger base unit will be used. Thus 604,800 seconds (7 days) returns "1W", not "7D".

All values above 31,622,400 (366 days) return "12M".

## Examples

```pinescript
//@version=6
indicator("HTF Close", "", true)
int chartTf = timeframe.in_seconds()
string tfTimes5 = timeframe.from_seconds(chartTf * 5)
float htfClose = request.security(syminfo.tickerid, tfTimes5, close)
plot(htfClose)
```

## See also

- [timeframe.in_seconds()](./in_seconds.md)
- [request.security](https://www.tradingview.com/pine-script-reference/v6/#var_request.security)
- [request.security_lower_tf](https://www.tradingview.com/pine-script-reference/v6/#var_request.security_lower_tf)
