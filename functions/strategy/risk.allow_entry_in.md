---
title: "strategy.risk.allow_entry_in"
kind: function
namespace: strategy
source: https://www.tradingview.com/pine-script-reference/v6/#fun_strategy.risk.allow_entry_in
---

# strategy.risk.allow_entry_in

**Category:** Function

## Syntax

```pinescript
strategy.risk.allow_entry_in(value) → void
```

## Description

This function can be used to specify in which market direction the [strategy.entry()](./entry.md) function is allowed to open positions.

## Arguments

- **`value`** `simple string` — The allowed direction. Possible values: [strategy.direction.all](../../constants/strategy/direction.all.md), [strategy.direction.long](../../constants/strategy/direction.long.md), [strategy.direction.short](../../constants/strategy/direction.short.md)

**Return type(s):** `void`

## Examples

```pinescript
//@version=6
strategy("strategy.risk.allow_entry_in")

strategy.risk.allow_entry_in(strategy.direction.long)
if open > close
	strategy.entry("Long", strategy.long)
// Instead of opening a short position with 10 contracts, this command will close long entries.
if open < close
	strategy.entry("Short", strategy.short, qty = 10)
```
