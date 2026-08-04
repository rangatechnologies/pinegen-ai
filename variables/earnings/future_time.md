---
title: "earnings.future_time"
kind: variable
namespace: earnings
source: https://www.tradingview.com/pine-script-reference/v6/#var_earnings.future_time
---

# earnings.future_time

**Category:** Variable

**Type:** `series int`

## Description

Returns a UNIX timestamp indicating the expected time of the next earnings report, or [na](../na.md) if this data isn't available.

## Returns

UNIX time, expressed in milliseconds.

## Remarks

This value is only fetched once during the script's initial calculation. The variable will return the same value until the script is recalculated, even after the expected time of the next earnings report.

## See also

- [request.earnings()](../../functions/request/earnings.md)
