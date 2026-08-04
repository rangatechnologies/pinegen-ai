---
title: "str.startswith"
kind: function
namespace: str
source: https://www.tradingview.com/pine-script-reference/v6/#fun_str.startswith
---

# str.startswith

**Category:** Function

## Syntax

_3 overloaded forms:_

```pinescript
str.startswith(source, str) → const bool
```

```pinescript
str.startswith(source, str) → simple bool
```

```pinescript
str.startswith(source, str) → series bool
```

## Description

Returns true if the `source` string starts with the substring specified in `str`, false otherwise.

## Arguments

- **`source`** `const string` — Source string.
- **`str`** `const string` — The substring to search for.

## Returns

True if the `source` string starts with the substring specified in `str`, false otherwise.

**Return type(s):** `const bool`

## See also

- [str.endswith()](./endswith.md)
