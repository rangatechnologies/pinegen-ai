---
title: "syminfo.root"
kind: variable
namespace: syminfo
source: https://www.tradingview.com/pine-script-reference/v6/#var_syminfo.root
---

# syminfo.root

**Category:** Variable

**Type:** `simple string`

## Description

Root for derivatives like futures contract. For other symbols returns the same value as [syminfo.ticker](./ticker.md).

## Examples

```pinescript
//@version=6
indicator("syminfo.root")

// If the current chart symbol is continuous futures ('ES1!'), it would display 'ES'.
if barstate.islastconfirmedhistory
	label.new(bar_index, high, syminfo.root)
```

## See also

- [syminfo.ticker](./ticker.md)
- [syminfo.tickerid](./tickerid.md)
