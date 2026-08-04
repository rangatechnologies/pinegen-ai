---
title: "@strategy_alert_message"
kind: annotation
source: https://www.tradingview.com/pine-script-reference/v6/#an_@strategy_alert_message
---

# @strategy_alert_message

**Category:** Annotation

## Description

If used within a [strategy()](../functions/strategy.md) script, it provides a default message to pre-fill the "Message" field in the alert creation dialogue.

## Examples

```pinescript
//@version=6
strategy("My strategy", overlay=true, margin_long=100, margin_short=100)
//@strategy_alert_message Strategy alert on symbol {{ticker}}

longCondition = ta.crossover(ta.sma(close, 14), ta.sma(close, 28))
if (longCondition)
    strategy.entry("My Long Entry Id", strategy.long)
strategy.exit("Exit", "My Long Entry Id", profit = 10 / syminfo.mintick, loss = 10 / syminfo.mintick)
```
