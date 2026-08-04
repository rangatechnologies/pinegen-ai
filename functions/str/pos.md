---
title: "str.pos"
kind: function
namespace: str
source: https://www.tradingview.com/pine-script-reference/v6/#fun_str.pos
---

# str.pos

**Category:** Function

## Syntax

_3 overloaded forms:_

```pinescript
str.pos(source, str) → const int
```

```pinescript
str.pos(source, str) → simple int
```

```pinescript
str.pos(source, str) → series int
```

## Description

Returns the position of the first occurrence of the `str` string in the `source` string, 'na' otherwise.

## Arguments

- **`source`** `const string` — Source string.
- **`str`** `const string` — The substring to search for.

## Returns

Position of the `str` string in the `source` string.

**Return type(s):** `const int`

## Remarks

Strings indexing starts at 0.

## See also

- [str.contains()](./contains.md)
- [str.match()](./match.md)
- [str.substring()](./substring.md)
