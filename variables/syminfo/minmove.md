---
title: "syminfo.minmove"
kind: variable
namespace: syminfo
source: https://www.tradingview.com/pine-script-reference/v6/#var_syminfo.minmove
---

# syminfo.minmove

**Category:** Variable

**Type:** `simple int`

## Description

Returns a whole number used to calculate the smallest increment between a symbol's price movements ([syminfo.mintick](./mintick.md)). It is the numerator in the [syminfo.mintick](./mintick.md) formula: `syminfo.minmove / syminfo.pricescale = syminfo.mintick`.

## See also

- [ticker.new()](../../functions/ticker/new.md)
- [syminfo.ticker](./ticker.md)
- [timeframe.period](../timeframe/period.md)
- [timeframe.multiplier](../timeframe/multiplier.md)
- [syminfo.root](./root.md)
