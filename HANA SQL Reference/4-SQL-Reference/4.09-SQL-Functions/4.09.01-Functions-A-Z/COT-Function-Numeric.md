# 4.9.1.45 COT Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 149–150

Computes the cotangent of a specified number.

## Syntax

```sql
COT(<number>)
```

## Description

Computes the cotangent of a number `<number>`, where `<number>` is an angle expressed in radians.

## Example

The following example returns the value `-0.8950829176379128` for `"cot"`:

```sql
SELECT COT (40) "cot" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
