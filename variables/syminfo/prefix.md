---
title: "syminfo.prefix"
kind: variable
namespace: syminfo
source: https://www.tradingview.com/pine-script-reference/v6/#var_syminfo.prefix
---

# syminfo.prefix

**Category:** Variable

**Type:** `simple string`

## Description

Prefix of current symbol name (i.e. for 'CME_EOD:TICKER' prefix is 'CME_EOD').

## Examples

```pinescript
//@version=6
indicator("syminfo.prefix")

// If current chart symbol is 'BATS:MSFT' then syminfo.prefix is 'BATS'.
if barstate.islastconfirmedhistory
	label.new(bar_index, high, text=syminfo.prefix)
```

## See also

- [syminfo.ticker](./ticker.md)
- [syminfo.tickerid](./tickerid.md)
