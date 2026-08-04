---
title: "last_bar_time"
kind: variable
source: https://www.tradingview.com/pine-script-reference/v6/#var_last_bar_time
---

# last_bar_time

**Category:** Variable

**Type:** `series int`

## Description

Time in UNIX format of the last chart bar. It is the number of milliseconds that have elapsed since 00:00:00 UTC, 1 January 1970.

## Remarks

Please note that using this variable/function can cause [indicator repainting](https://www.tradingview.com/pine-script-docs/concepts/repainting/).

Note that this variable returns the timestamp based on the time of the bar's open.

## See also

- [time](./time.md)
- [timenow](./timenow.md)
- [timestamp()](../functions/timestamp.md)
- [last_bar_index](./last_bar_index.md)
