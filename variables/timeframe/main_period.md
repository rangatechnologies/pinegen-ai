---
title: "timeframe.main_period"
kind: variable
namespace: timeframe
source: https://www.tradingview.com/pine-script-reference/v6/#var_timeframe.main_period
---

# timeframe.main_period

**Category:** Variable

**Type:** `simple string`

## Description

A string representation of the script's main timeframe. If the script is an [indicator()](../../functions/indicator.md) that specifies a `timeframe` value in its declaration statement, this variable holds that value. Otherwise, its value represents the chart's timeframe. Unlike [timeframe.period](./period.md), this variable's value does not change when used in the `expression` argument of a `request.*()` function call.

The string's format is "<quantity>[<unit>]", where <unit> is "T" for ticks, "S" for seconds, "D" for days, "W" for weeks, and "M" for months, but is absent for minutes. No <unit> exists for hours: hourly timeframes are expressed in minutes.

The variable's value is: "10S" for 10 seconds, "30" for 30 minutes, "240" for four hours, "1D" for one day, "2W" for two weeks, and "3M" for one quarter.

## See also

- [timeframe.period](./period.md)
- [syminfo.main_tickerid](../syminfo/main_tickerid.md)
- [syminfo.ticker](../syminfo/ticker.md)
- [syminfo.tickerid](../syminfo/tickerid.md)
- [timeframe.multiplier](./multiplier.md)
