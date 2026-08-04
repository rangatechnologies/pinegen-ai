---
title: "syminfo.volumetype"
kind: variable
namespace: syminfo
source: https://www.tradingview.com/pine-script-reference/v6/#var_syminfo.volumetype
---

# syminfo.volumetype

**Category:** Variable

**Type:** `simple string`

## Description

Volume type of the current symbol. Possible values are: "base" for base currency, "quote" for quote currency, "tick" for the number of transactions, and "n/a" when there is no volume or its type is not specified.

## Remarks

Only some data feed suppliers provide information qualifying volume. As a result, the variable will return a value on some symbols only, mostly in the crypto sector.

## See also

- [syminfo.type](./type.md)
