---
title: "syminfo.ticker"
kind: function
namespace: syminfo
source: https://www.tradingview.com/pine-script-reference/v6/#fun_syminfo.ticker
---

# syminfo.ticker

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
syminfo.ticker(symbol) → simple string
```

```pinescript
syminfo.ticker(symbol) → series string
```

## Description

Returns `symbol` name without exchange prefix, e.g. "AAPL".

## Arguments

- **`symbol`** `simple string` — Symbol. Note that the symbol should be passed with a prefix. For example: "NASDAQ:AAPL" instead of "AAPL".

## Returns

Returns `symbol` name without exchange prefix, e.g. "AAPL".

**Return type(s):** `simple string`

## Remarks

The result of the function is used in the [ticker.new()](../ticker/new.md)/[ticker.modify()](../ticker/modify.md) and [request.security()](../request/security.md).

## Examples

```pinescript
//@version=6
indicator("syminfo.ticker fun", overlay=true)
i_sym = input.symbol("NASDAQ:AAPL")
pref = syminfo.prefix(i_sym)
tick = syminfo.ticker(i_sym)
t = ticker.new(pref, tick, session.extended)
s = request.security(t, "1D", close)
plot(s)
```

## See also

- [syminfo.tickerid](../../variables/syminfo/tickerid.md)
- [syminfo.ticker](../../variables/syminfo/ticker.md)
- [syminfo.prefix](../../variables/syminfo/prefix.md)
- [syminfo.prefix()](./prefix.md)
- [ticker.new()](../ticker/new.md)
