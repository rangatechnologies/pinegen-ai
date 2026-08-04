---
title: "syminfo.main_tickerid"
kind: variable
namespace: syminfo
source: https://www.tradingview.com/pine-script-reference/v6/#var_syminfo.main_tickerid
---

# syminfo.main_tickerid

**Category:** Variable

**Type:** `simple string`

## Description

A ticker identifier representing the current chart's symbol. The value contains an exchange prefix and a symbol name, separated by a colon (e.g., "NASDAQ:AAPL"). It can also include information about data modifications such as dividend adjustment, non-standard chart type, currency conversion, etc. Unlike [syminfo.tickerid](./tickerid.md), this variable's value does not change when used in the `expression` argument of a `request.*()` function call.

## See also

- [ticker.new()](../../functions/ticker/new.md)
- [timeframe.main_period](../timeframe/main_period.md)
- [syminfo.tickerid](./tickerid.md)
- [syminfo.ticker](./ticker.md)
- [timeframe.period](../timeframe/period.md)
- [timeframe.multiplier](../timeframe/multiplier.md)
- [syminfo.root](./root.md)
