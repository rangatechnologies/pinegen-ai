---
title: "year"
kind: variable
source: https://www.tradingview.com/pine-script-reference/v6/#var_year
---

# year

**Category:** Variable

**Type:** `series int`

## Description

Current bar year in exchange timezone.

## Remarks

Note that this variable returns the year based on the time of the bar's open. For overnight sessions (e.g. EURUSD, where Monday session starts on Sunday, 17:00) this value can be lower by 1 than the year of the trading day.

## See also

- [year()](../functions/year.md)
- [time](./time.md)
- [month](./month.md)
- [weekofyear](./weekofyear.md)
- [dayofmonth](./dayofmonth.md)
- [dayofweek](./dayofweek.md)
- [hour](./hour.md)
- [minute](./minute.md)
- [second](./second.md)
