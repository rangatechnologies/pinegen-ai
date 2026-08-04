---
title: "dividends.future_ex_date"
kind: variable
namespace: dividends
source: https://www.tradingview.com/pine-script-reference/v6/#var_dividends.future_ex_date
---

# dividends.future_ex_date

**Category:** Variable

**Type:** `series int`

## Description

Returns the Ex-dividend date (Ex-date) of the current instrument's next dividend payment, or [na](../na.md) if this data isn't available. Ex-dividend date signifies when investors are no longer entitled to a payout from the most recent dividend. Only those who purchased shares before this day are entitled to the dividend payment.

## Returns

UNIX time, expressed in milliseconds.

## Remarks

This value is only fetched once during the script's initial calculation. The variable will return the same value until the script is recalculated, even after the expected Payment date of the next dividend.
