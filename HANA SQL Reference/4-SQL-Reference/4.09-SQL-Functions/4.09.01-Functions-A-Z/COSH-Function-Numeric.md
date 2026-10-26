# 4.9.1.44 COSH Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 148–149

Computes the hyperbolic cosine of the specified argument.

## Syntax

```sql
COSH(<number>)
```

## Description

Computes the hyperbolic cosine of the numeric argument `<number>`.

## Example

The following example returns the value `1.1276259652063807` for `"cosh"`:

```sql
SELECT COSH (0.5) "cosh" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
