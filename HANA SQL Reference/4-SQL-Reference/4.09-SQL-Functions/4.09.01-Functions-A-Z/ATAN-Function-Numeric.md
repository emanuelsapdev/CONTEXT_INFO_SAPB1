# 4.9.1.17 ATAN Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 102–103

Returns the arc-tangent, in radians, of a numeric argument.

## Syntax

```sql
ATAN(<number>)
```

## Syntax Elements

**number** Specifies a numeric argument.

## Description

Returns the arc-tangent, in radians, of the numeric argument `<number>`. The range of `<number>` is unlimited.

## Example

The following example returns the value `0.4636476090008061` for `"atan"`:

```sql
SELECT ATAN (0.5) "atan" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
