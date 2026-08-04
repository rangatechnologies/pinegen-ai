---
title: "barmerge.lookahead_on"
kind: constant
namespace: barmerge
source: https://www.tradingview.com/pine-script-reference/v6/#const_barmerge.lookahead_on
---

# barmerge.lookahead_on

**Category:** Constant

**Type:** `const barmerge_lookahead`

## Description

Merge strategy for the requested data position. Requested barset is merged with current barset in the order of sorting bars by their opening time. This merge strategy can lead to undesirable effect of getting data from "future" on calculation on history. This is unacceptable in backtesting strategies, but can be useful in indicators.

## See also

- [request.security()](../../functions/request/security.md)
- [barmerge.lookahead_off](./lookahead_off.md)
