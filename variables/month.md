---
title: "month"
kind: variable
source: https://www.tradingview.com/pine-script-reference/v6/#var_month
---

# month

**Category:** Variable

**Type:** `series int`

## Description

Current bar month in exchange timezone.

## Remarks

Note that this variable returns the month based on the time of the bar's open. For overnight sessions (e.g. EURUSD, where Monday session starts on Sunday, 17:00) this value can be lower by 1 than the month of the trading day.

## See also

- [month()](../functions/month.md)
- [time](./time.md)
- [year](./year.md)
- [weekofyear](./weekofyear.md)
- [dayofmonth](./dayofmonth.md)
- [dayofweek](./dayofweek.md)
- [hour](./hour.md)
- [minute](./minute.md)
- [second](./second.md)
