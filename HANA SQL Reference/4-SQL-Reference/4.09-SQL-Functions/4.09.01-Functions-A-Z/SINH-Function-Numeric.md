# 4.9.1.178 SINH Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 330–331

Returns the hyperbolic sine of an angle expressed in radians.

## Syntax

```sql
SINH(<number>)
```

## Description

Returns the hyperbolic sine of `<number>`, where the argument is an angle expressed in radians.

## Example

The following example returns the value `0` for `"sinh"`:

```sql
SELECT SINH (0.0) "sinh" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
