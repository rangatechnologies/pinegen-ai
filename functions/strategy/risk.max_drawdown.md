---
title: "strategy.risk.max_drawdown"
kind: function
namespace: strategy
source: https://www.tradingview.com/pine-script-reference/v6/#fun_strategy.risk.max_drawdown
---

# strategy.risk.max_drawdown

**Category:** Function

## Syntax

```pinescript
strategy.risk.max_drawdown(value, type, alert_message) → void
```

## Description

The purpose of this rule is to determine maximum drawdown. The rule affects the whole strategy. Once the maximum drawdown value is reached, all pending orders are cancelled, all open positions are closed and no new orders can be placed.

## Arguments

- **`value`** `simple int/float` — A required parameter. The maximum drawdown value. It is specified either in money (base currency), or in percentage of maximum equity. For % of equity the range of allowed values is from 0 to 100.
- **`type`** `simple string` — A required parameter. The type of the value. Please specify one of the following values: [strategy.percent_of_equity](../../constants/strategy/percent_of_equity.md) or [strategy.cash](../../constants/strategy/cash.md). Note: if equity drops down to zero or to a negative and the 'strategy.percent_of_equity' is specified, all pending orders are cancelled, all open positions are closed and no new orders can be placed for good.
- **`alert_message`** `simple string` (optional) — An optional parameter which replaces the {{strategy.order.alert_message}} placeholder when it is used in the "Create Alert" dialog box's "Message" field.

**Return type(s):** `void`

## Detailed Description



```pinescript
//@version=6
strategy("risk.max_drawdown Demo 1")
strategy.risk.max_drawdown(50, strategy.percent_of_equity) // set maximum drawdown to 50% of maximum equity
plot(strategy.position_size)
```

---



```pinescript
//@version=6
strategy("risk.max_drawdown Demo 2", currency = "EUR")
strategy.risk.max_drawdown(2000, strategy.cash) // set maximum drawdown to 2000 EUR from maximum equity
plot(strategy.position_size)
```
