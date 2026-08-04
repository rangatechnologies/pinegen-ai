---
title: "strategy.opentrades.profit_percent"
kind: function
namespace: strategy
source: https://www.tradingview.com/pine-script-reference/v6/#fun_strategy.opentrades.profit_percent
---

# strategy.opentrades.profit_percent

**Category:** Function

## Syntax

```pinescript
strategy.opentrades.profit_percent(trade_num) → series float
```

## Description

Returns the profit/loss of the open trade, expressed as a percentage. Losses are expressed as negative values.

## Arguments

- **`trade_num`** `series int` — The trade number of the closed trade. The number of the first trade is zero.

**Return type(s):** `series float`

## See also

- [strategy.opentrades.profit()](./opentrades.profit.md)
