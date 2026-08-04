---
title: "dividends.future_pay_date"
kind: variable
namespace: dividends
source: https://www.tradingview.com/pine-script-reference/v6/#var_dividends.future_pay_date
---

# dividends.future_pay_date

**Category:** Variable

**Type:** `series int`

## Description

Returns the Payment date (Pay date) of the current instrument's next dividend payment, or [na](../na.md) if this data isn't available. Payment date signifies the day when eligible investors will receive the dividend payment.

## Returns

UNIX time, expressed in milliseconds.

## Remarks

This value is only fetched once during the script's initial calculation. The variable will return the same value until the script is recalculated, even after the expected Payment date of the next dividend.
