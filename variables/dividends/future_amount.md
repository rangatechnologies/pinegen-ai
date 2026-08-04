---
title: "dividends.future_amount"
kind: variable
namespace: dividends
source: https://www.tradingview.com/pine-script-reference/v6/#var_dividends.future_amount
---

# dividends.future_amount

**Category:** Variable

**Type:** `series float`

## Description

Returns the payment amount of the upcoming dividend in the currency of the current instrument, or [na](../na.md) if this data isn't available.

## Remarks

This value is only fetched once during the script's initial calculation. The variable will return the same value until the script is recalculated, even after the expected Payment date of the next dividend.
