---
title: "strategy.risk.max_cons_loss_days"
kind: function
namespace: strategy
source: https://www.tradingview.com/pine-script-reference/v6/#fun_strategy.risk.max_cons_loss_days
---

# strategy.risk.max_cons_loss_days

**Category:** Function

## Syntax

```pinescript
strategy.risk.max_cons_loss_days(count, alert_message) → void
```

## Description

The purpose of this rule is to cancel all pending orders, close all open positions and stop placing orders after a specified number of consecutive days with losses. The rule affects the whole strategy.

## Arguments

- **`count`** `simple int` — A required parameter. The allowed number of consecutive days with losses.
- **`alert_message`** `simple string` (optional) — An optional parameter which replaces the {{strategy.order.alert_message}} placeholder when it is used in the "Create Alert" dialog box's "Message" field.

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
strategy("risk.max_cons_loss_days Demo 1")
strategy.risk.max_cons_loss_days(3) // No orders will be placed after 3 days, if each day is with loss.
plot(strategy.position_size)
```
