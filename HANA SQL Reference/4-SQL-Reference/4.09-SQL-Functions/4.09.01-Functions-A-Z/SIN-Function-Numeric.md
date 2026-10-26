# 4.9.1.177 SIN Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 330

Returns the sine of an angle expressed in radians.

## Syntax

```sql
SIN(<number>)
```

## Description

Returns the sine of `<number>`, where `<number>` is an angle expressed in radians.

## Example

The following example returns the value `1.0` for `"sine"`:

```sql
SELECT SIN ( 3.141592653589793/2) "sine" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
