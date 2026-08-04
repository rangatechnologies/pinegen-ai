---
title: "strategy.oca.reduce"
kind: constant
namespace: strategy
source: https://www.tradingview.com/pine-script-reference/v6/#const_strategy.oca.reduce
---

# strategy.oca.reduce

**Category:** Constant

**Type:** `const string`

## Description

A named constant for use with the `oca_type` parameter of the [strategy.entry()](../../functions/strategy/entry.md) and [strategy.order()](../../functions/strategy/order.md) commands. It specifies that when another order with the same `oca_name` and `oca_type` executes, the strategy reduces the unfilled order by that order's size. If the unfilled order's size reaches 0 after reduction, it is the same as canceling the order entirely.

## Remarks

Strategies cannot cancel or reduce pending orders from an OCA group if they execute on the same tick. For example, if the market price triggers two stop orders from [strategy.order()](../../functions/strategy/order.md) calls with the same `oca_*` arguments, the strategy cannot fully or partially cancel either one.

Orders from [strategy.exit()](../../functions/strategy/exit.md) automatically use this OCA type, and they belong to the same OCA group by default.

## See also

- [strategy.entry()](../../functions/strategy/entry.md)
- [strategy.exit()](../../functions/strategy/exit.md)
- [strategy.order()](../../functions/strategy/order.md)
