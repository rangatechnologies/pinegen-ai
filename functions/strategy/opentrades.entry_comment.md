---
title: "strategy.opentrades.entry_comment"
kind: function
namespace: strategy
source: https://www.tradingview.com/pine-script-reference/v6/#fun_strategy.opentrades.entry_comment
---

# strategy.opentrades.entry_comment

**Category:** Function

## Syntax

```pinescript
strategy.opentrades.entry_comment(trade_num) → series string
```

## Description

Returns the comment message of the open trade's entry, or [na](../../variables/na.md) if there is no entry with this `trade_num`.

## Arguments

- **`trade_num`** `series int` — The trade number of the open trade. The number of the first trade is zero.

**Return type(s):** `series string`

## Examples

```pinescript
//@version=6
strategy("`strategy.opentrades.entry_comment()` Example", overlay = true)

stopPrice = open * 1.01

longCondition = ta.crossover(ta.sma(close, 14), ta.sma(close, 28))

if (longCondition)
    strategy.entry("Long", strategy.long, stop = stopPrice, comment = str.tostring(stopPrice, "#.####"))

var testTable = table.new(position.top_right, 1, 3, color.orange, border_width = 1)

if barstate.islastconfirmedhistory or barstate.isrealtime
    table.cell(testTable, 0, 0, 'Last entry stats')
    table.cell(testTable, 0, 1, "Order stop price value: " + strategy.opentrades.entry_comment(strategy.opentrades - 1))
    table.cell(testTable, 0, 2, "Actual Entry Price: " + str.tostring(strategy.opentrades.entry_price(strategy.opentrades - 1)))
```

## See also

- [strategy()](../strategy.md)
- [strategy.entry()](./entry.md)
- [strategy.opentrades](../../variables/strategy/opentrades.md)
