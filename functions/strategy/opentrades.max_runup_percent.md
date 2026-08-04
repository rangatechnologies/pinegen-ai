---
title: "strategy.opentrades.max_runup_percent"
kind: function
namespace: strategy
source: https://www.tradingview.com/pine-script-reference/v6/#fun_strategy.opentrades.max_runup_percent
---

# strategy.opentrades.max_runup_percent

**Category:** Function

## Syntax

```pinescript
strategy.opentrades.max_runup_percent(trade_num) → series float
```

## Description

Returns the maximum run-up of the open trade, i.e., the maximum possible profit during the trade, expressed as a percentage and calculated by formula: `Highest Value During Trade / (Entry Price x Quantity) * 100`.

## Arguments

- **`trade_num`** `series int` — The trade number of the closed trade. The number of the first trade is zero.

**Return type(s):** `series float`

## See also

- [strategy.opentrades.max_runup()](./opentrades.max_runup.md)
- [strategy.max_runup](../../variables/strategy/max_runup.md)
