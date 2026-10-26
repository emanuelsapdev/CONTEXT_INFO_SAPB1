# 4.9.1.180 SQRT Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 332–333

Returns the square root of the specified argument.

## Syntax

```sql
SQRT(<number>)
```

## Description

Returns the square root of the numeric argument `<number>`.

## Example

The following example returns the value `1.4142135623730951` for `"sqrt"`:

```sql
SELECT SQRT (2) "sqrt" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
