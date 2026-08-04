---
title: "timeframe.in_seconds"
kind: function
namespace: timeframe
source: https://www.tradingview.com/pine-script-reference/v6/#fun_timeframe.in_seconds
---

# timeframe.in_seconds

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
timeframe.in_seconds(timeframe) → simple int
```

```pinescript
timeframe.in_seconds(timeframe) → series int
```

## Description

Converts a timeframe string into seconds.

## Arguments

- **`timeframe`** `simple string` (optional) — Timeframe string in [timeframe string specifications](https://www.tradingview.com/pine-script-docs/concepts/timeframes/#timeframe-string-specifications) format. Optional. The default is [timeframe.period](../../variables/timeframe/period.md).

## Returns

The "int" representation of the number of seconds in the timeframe string.

**Return type(s):** `simple int`

## Remarks

When the timeframe is "1M" or more, calculations use 2628003 as the number of seconds in one month, which represents 30.4167 (365/12) days.

## Examples

```pinescript
//@version=6
indicator("`timeframe_in_seconds()`"),

// Get a user-selected timeframe.
tfInput = input.timeframe("1D")

// Convert it into an "int" number of seconds.
secondsInTf = timeframe.in_seconds(tfInput)

plot(secondsInTf)
```

## See also

- [input.timeframe()](../input/timeframe.md)
- [timeframe.period](../../variables/timeframe/period.md)
- [timeframe.from_seconds()](./from_seconds.md)
