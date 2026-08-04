---
title: "str.endswith"
kind: function
namespace: str
source: https://www.tradingview.com/pine-script-reference/v6/#fun_str.endswith
---

# str.endswith

**Category:** Function

## Syntax

_3 overloaded forms:_

```pinescript
str.endswith(source, str) → const bool
```

```pinescript
str.endswith(source, str) → simple bool
```

```pinescript
str.endswith(source, str) → series bool
```

## Description

Returns true if the `source` string ends with the substring specified in `str`, false otherwise.

## Arguments

- **`source`** `const string` — Source string.
- **`str`** `const string` — The substring to search for.

## Returns

True if the `source` string ends with the substring specified in `str`, false otherwise.

**Return type(s):** `const bool`

## See also

- [str.startswith()](./startswith.md)
