---
title: "@version="
kind: annotation
source: https://www.tradingview.com/pine-script-reference/v6/#an_@version=
---

# @version=

**Category:** Annotation

## Description

Specifies the Pine Script® version that the script will use. The number in this annotation should not be confused with the script's version number, which updates on every saved change to the code.

## Remarks

The version should always be specified. Otherwise, for compatibility reasons, the script will be compiled using Pine Script® v1, which lacks most of the newer features and is bound to confuse. This annotation can be anywhere within a script, but we recommend placing it at the top of the code for readability.

## Detailed Description



```pinescript
//@version=6
indicator("Pine v6 Indicator")
plot(close)
```

---



```pinescript
//This indicator has no version annotation, so it will try to use v1.
//Pine Script® v1 has no function named `indicator()`, so the script will not compile.
indicator("Pine v1 Indicator")
plot(close)
```
