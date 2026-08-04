---
title: "format.mintick"
kind: constant
namespace: format
source: https://www.tradingview.com/pine-script-reference/v6/#const_format.mintick
---

# format.mintick

**Category:** Constant

**Type:** `const string`

## Description

Is a named constant to use with the [str.tostring()](../../functions/str/tostring.md) function. Passing a number to [str.tostring()](../../functions/str/tostring.md) with this argument rounds the number to the nearest value that can be divided by [syminfo.mintick](../../variables/syminfo/mintick.md), without the remainder, with ties rounding up, and returns the string version of said value with trailing zeros.

## See also

- [indicator()](../../functions/indicator.md)
- [format.inherit](./inherit.md)
- [format.price](./price.md)
- [format.volume](./volume.md)
