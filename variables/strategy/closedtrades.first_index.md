---
title: "strategy.closedtrades.first_index"
kind: variable
namespace: strategy
source: https://www.tradingview.com/pine-script-reference/v6/#var_strategy.closedtrades.first_index
---

# strategy.closedtrades.first_index

**Category:** Variable

**Type:** `series int`

## Description

The index, or trade number, of the first (oldest) trade listed in the List of Trades. This number is usually zero. If more trades than the allowed limit have been closed, the oldest trades are removed, and this number is the index of the oldest remaining trade.

## See also

- [strategy.position_size](./position_size.md)
- [strategy.opentrades](./opentrades.md)
- [strategy.wintrades](./wintrades.md)
- [strategy.losstrades](./losstrades.md)
- [strategy.eventrades](./eventrades.md)
