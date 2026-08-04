---
title: "format.volume"
kind: constant
namespace: format
source: https://www.tradingview.com/pine-script-reference/v6/#const_format.volume
---

# format.volume

**Category:** Constant

**Type:** `const string`

## Description

Is a named constant for selecting the formatting of the script output values as volume in the [indicator()](../../functions/indicator.md) function, e.g. '5183' will be formatted as '5.183K'.

The decimal precision rules defined by this variable take precedence over other precision settings. When an [indicator()](../../functions/indicator.md), [strategy()](../../functions/strategy.md), or `plot*()` call uses this `format` option, the function's `precision` parameter will not affect the result.

## See also

- [indicator()](../../functions/indicator.md)
- [format.inherit](./inherit.md)
- [format.price](./price.md)
- [format.percent](./percent.md)
