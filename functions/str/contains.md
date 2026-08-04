---
title: "str.contains"
kind: function
namespace: str
source: https://www.tradingview.com/pine-script-reference/v6/#fun_str.contains
---

# str.contains

**Category:** Function

## Syntax

_3 overloaded forms:_

```pinescript
str.contains(source, str) → const bool
```

```pinescript
str.contains(source, str) → simple bool
```

```pinescript
str.contains(source, str) → series bool
```

## Description

Returns true if the `source` string contains the `str` substring, false otherwise.

## Arguments

- **`source`** `const string` — Source string.
- **`str`** `const string` — The substring to search for.

## Returns

True if the `str` was found in the `source` string, false otherwise.

**Return type(s):** `const bool`

## Examples

```pinescript
//@version=6
indicator("str.contains")
// If the current chart is a continuous futures chart, e.g “BTC1!”, then the function will return true, false otherwise.
var isFutures = str.contains(syminfo.tickerid, "!")
plot(isFutures ? 1 : 0)
```

## See also

- [str.pos()](./pos.md)
- [str.match()](./match.md)
