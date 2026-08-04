---
title: "strategy.opentrades.entry_id"
kind: function
namespace: strategy
source: https://www.tradingview.com/pine-script-reference/v6/#fun_strategy.opentrades.entry_id
---

# strategy.opentrades.entry_id

**Category:** Function

## Syntax

```pinescript
strategy.opentrades.entry_id(trade_num) → series string
```

## Description

Returns the id of the open trade's entry.

## Arguments

- **`trade_num`** `series int` — The trade number of the open trade. The number of the first trade is zero.

## Returns

Returns the id of the open trade's entry.

**Return type(s):** `series string`

## Remarks

The function returns na if trade_num is not in the range: 0 to strategy.opentrades-1.

## Examples

```pinescript
//@version=6
strategy("`strategy.opentrades.entry_id` Example", overlay = true)

// We enter a long position when 14 period sma crosses over 28 period sma.
// We enter a short position when 14 period sma crosses under 28 period sma.
longCondition = ta.crossover(ta.sma(close, 14), ta.sma(close, 28))
shortCondition = ta.crossunder(ta.sma(close, 14), ta.sma(close, 28))

// Strategy calls to enter a long or short position when the corresponding condition is met.
if longCondition
    strategy.entry("Long entry at bar #" + str.tostring(bar_index), strategy.long)
if shortCondition
    strategy.entry("Short entry at bar #" + str.tostring(bar_index), strategy.short)

// Display ID of the latest open position.
if barstate.islastconfirmedhistory
    label.new(bar_index, high + (2 * ta.tr), "Last opened position is \n " + strategy.opentrades.entry_id(strategy.opentrades - 1))
```

## See also

- [strategy.opentrades.entry_bar_index()](./opentrades.entry_bar_index.md)
- [strategy.opentrades.entry_price()](./opentrades.entry_price.md)
- [strategy.opentrades.entry_time()](./opentrades.entry_time.md)
