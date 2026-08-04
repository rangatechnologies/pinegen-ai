---
title: "earnings.future_period_end_time"
kind: variable
namespace: earnings
source: https://www.tradingview.com/pine-script-reference/v6/#var_earnings.future_period_end_time
---

# earnings.future_period_end_time

**Category:** Variable

**Type:** `series int`

## Description

Checks the data for the next earnings report and returns the UNIX timestamp of the day when the financial period covered by those earnings ends, or [na](../na.md) if this data isn't available.

## Returns

UNIX time, expressed in milliseconds.

## Remarks

This value is only fetched once during the script's initial calculation. The variable will return the same value until the script is recalculated, even after the expected time of the next earnings report.

## See also

- [request.earnings()](../../functions/request/earnings.md)
