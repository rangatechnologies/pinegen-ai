---
title: "syminfo.tickerid"
kind: variable
namespace: syminfo
source: https://www.tradingview.com/pine-script-reference/v6/#var_syminfo.tickerid
---

# syminfo.tickerid

**Category:** Variable

**Type:** `simple string`

## Description

A ticker identifier representing the chart's symbol or a requested symbol, depending on how the script uses it. The variable's value represents a requested dataset's ticker ID when used in the `expression` argument of a `request.*()` function call. Otherwise, it represents the chart's ticker ID. The value contains an exchange prefix and a symbol name, separated by a colon (e.g., "NASDAQ:AAPL"). It can also include information about data modifications such as dividend adjustment, non-standard chart type, currency conversion, etc.

## Remarks

Because the value of this variable does not always use a simple "prefix:ticker" format, it is a poor candidate for use in boolean comparisons or string manipulation functions. In those contexts, run the variable's result through [ticker.standard()](../../functions/ticker/standard.md) to purify it. This will remove any extraneous information and return a ticker ID consistently formatted using the "prefix:ticker" structure.

To always access the script's main ticker ID, even within another context, use the [syminfo.main_tickerid](./main_tickerid.md) variable.

## See also

- [ticker.new()](../../functions/ticker/new.md)
- [syminfo.main_tickerid](./main_tickerid.md)
- [timeframe.main_period](../timeframe/main_period.md)
- [syminfo.ticker](./ticker.md)
- [timeframe.period](../timeframe/period.md)
- [timeframe.multiplier](../timeframe/multiplier.md)
- [syminfo.root](./root.md)
