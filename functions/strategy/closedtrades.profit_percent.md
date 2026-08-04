---
title: "strategy.closedtrades.profit_percent"
kind: function
namespace: strategy
source: https://www.tradingview.com/pine-script-reference/v6/#fun_strategy.closedtrades.profit_percent
---

# strategy.closedtrades.profit_percent

**Category:** Function

## Syntax

```pinescript
strategy.closedtrades.profit_percent(trade_num) → series float
```

## Description

Returns the profit/loss value of the closed trade, expressed as a percentage. Losses are expressed as negative values.

## Arguments

- **`trade_num`** `series int` — The trade number of the closed trade. The number of the first trade is zero.

**Return type(s):** `series float`

## See also

- [strategy.closedtrades.profit()](./closedtrades.profit.md)
