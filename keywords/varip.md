---
title: "varip"
kind: keyword
source: https://www.tradingview.com/pine-script-reference/v6/#kw_varip
---

# varip

**Category:** Keyword

## Syntax

```pinescript
varip [<variable_type> ]<variable_name> = <expression>

[export ]type <UDT_identifier>
    varip <field_type> <field_name> [= <value>]
```

## Description

**varip** (var intrabar persist) is the keyword used for the assignment and one-time initialization of a variable or a field of a user-defined [type](./type.md). It’s similar to the [var](./var.md) keyword, but variables and fields declared with [varip](./varip.md) retain their values between executions of the script on the same bar.

## Remarks

When using [varip](./varip.md) to declare variables in strategies that may execute more than once per historical chart bar, the values of such variables are preserved across successive iterations of the script on the same bar.

The effect of [varip](./varip.md) eliminates the [rollback](https://www.tradingview.com/pine-script-docs/language/execution-model/#calculation-based-on-realtime-bars) of variables before each successive execution of a script on the same bar.

## Detailed Description

where:

**variable_type** - An optional fundamental type ([int](../types/int.md), [float](../types/float.md), [bool](../types/bool.md), [color](../types/color.md), [string](../types/string.md)) or a user-defined type, or an array or matrix of one of those types. Special types are not compatible with this keyword.

**variable_name** - A [valid identifier](https://www.tradingview.com/pine-script-docs/language/identifiers/). The variable can also be an object created from a UDT.

**expression** - Any arithmetic expression, just as when defining a regular variable. The expression will be calculated and assigned to the variable only once, on the first bar.

**UDT_identifier, field_type, field_name, value** - Constructs related to user-defined types as described in the [type](./type.md) section.

```pinescript
//@version=6
indicator("varip")
varip int v = -1
v := v + 1
plot(v)
```

---

With [var](./var.md), `v` would equal the value of the [bar_index](../variables/bar_index.md). On historical bars, where the script calculates only once per chart bar, the value of `v` is the same as with [var](./var.md). However, on realtime bars, the script will evaluate the expression on each new chart update, producing a different result.

```pinescript
//@version=6
indicator("varip with types")
type barData
    int index = -1
    varip int ticks = -1

var currBar = barData.new()
currBar.index += 1
currBar.ticks += 1

// Will be equal to bar_index on all bars
plot(currBar.index)
// In real time, will increment per every tick on the chart
plot(currBar.ticks)
```

---

The same [+=](../operators/add-assign.md) operation applied to both the `index` and `ticks` fields results in different real-time values because `ticks` increases on every chart update, while `index` only does so once per bar. Note how the `currBar` object does not use the [varip](./varip.md) keyword. The `ticks` field of the object can increment on every tick, but the reference itself is defined once and then stays unchanged. If we were to declare `currBar` using [varip](./varip.md), the behavior of `index` would remain unchanged because while the reference to the type instance would persist between chart updates, the `index` field of the object would not.
