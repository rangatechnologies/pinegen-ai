---
title: "syminfo.prefix"
kind: function
namespace: syminfo
source: https://www.tradingview.com/pine-script-reference/v6/#fun_syminfo.prefix
---

# syminfo.prefix

**Category:** Function

## Syntax

_2 overloaded forms:_

```pinescript
syminfo.prefix(symbol) → simple string
```

```pinescript
syminfo.prefix(symbol) → series string
```

## Description

Returns exchange prefix of the `symbol`, e.g. "NASDAQ".

## Arguments

- **`symbol`** `simple string` — Symbol. Note that the symbol should be passed with a prefix. For example: "NASDAQ:AAPL" instead of "AAPL".

## Returns

Returns exchange prefix of the `symbol`, e.g. "NASDAQ".

**Return type(s):** `simple string`

## Remarks

The result of the function is used in the [ticker.new()](../ticker/new.md)/[ticker.modify()](../ticker/modify.md) and [request.security()](../request/security.md).

## Examples

```pinescript
//@version=6
indicator("syminfo.prefix fun", overlay=true)
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
- [syminfo.ticker()](./ticker.md)
- [ticker.new()](../ticker/new.md)
