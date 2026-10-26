# 4.9.1.193 TAN Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 348–349

Returns the tangent of a specified number, where the argument is an angle expressed in radians.

## Syntax

```sql
TAN(<number>)
```

## Description

Returns the tangent of `<number>`, where `<n>` is an angle expressed in radians.

## Example

The following example returns the value `0` for `"tan"`:

```sql
SELECT TAN (0.0) "tan" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
