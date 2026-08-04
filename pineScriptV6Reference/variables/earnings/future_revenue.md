---
title: "earnings.future_revenue"
kind: variable
namespace: earnings
source: https://www.tradingview.com/pine-script-reference/v6/#var_earnings.future_revenue
---

# earnings.future_revenue

**Category:** Variable

**Type:** `series float`

## Description

Returns the estimated Revenue of the next earnings report in the currency of the instrument, or [na](../na.md) if this data isn't available.

## Remarks

This value is only fetched once during the script's initial calculation. The variable will return the same value until the script is recalculated, even after the expected time of the next earnings report.

## See also

- [request.earnings()](../../functions/request/earnings.md)
