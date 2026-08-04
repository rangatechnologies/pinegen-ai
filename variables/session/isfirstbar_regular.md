---
title: "session.isfirstbar_regular"
kind: variable
namespace: session
source: https://www.tradingview.com/pine-script-reference/v6/#var_session.isfirstbar_regular
---

# session.isfirstbar_regular

**Category:** Variable

**Type:** `series bool`

## Description

Returns [true](../../constants/true.md) on the first regular session bar of the day, [false](../../constants/false.md) otherwise. The result is the same whether extended session information is used or not.

## Examples

```pinescript
//@version=6
strategy("`session.isfirstbar_regular` Example", overlay = true)
longCondition = year >= 2022
// Place a long order at the `close` of the trading session's first bar.
if session.isfirstbar and longCondition
    strategy.entry("Long", strategy.long)
// Close the long position at the `close` of the trading session's last bar.
if session.islastbar_regular and barstate.isconfirmed
    strategy.close("Long", immediately = true)
```

## See also

- [session.isfirstbar](./isfirstbar.md)
- [session.islastbar](./islastbar.md)
