# 4.9.1.43 COS Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 148

Returns the cosine of the angle, in radians, for the specified argument.

## Syntax

```sql
COS(<number>)
```

## Description

Returns the cosine of the angle `<number>`, in radians.

## Example

The following example returns the value `1.0` for `"cos"`:

```sql
SELECT COS (0.0) "cos" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
