# 4.9.1.176 SIGN Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 329–330

Returns the sign (positive or negative) of the specified numeric argument.

## Syntax

```sql
SIGN(<number>)
```

## Description

Returns 1 if `<number>` is a positive value, -1 if `<number>` is a negative value, 0 if `<number>` is equal to zero, and NULL if `<number>` is equal to NULL.

## Example

The following example returns the value `-1` for `"sign"`:

```sql
SELECT SIGN (-15) "sign" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
