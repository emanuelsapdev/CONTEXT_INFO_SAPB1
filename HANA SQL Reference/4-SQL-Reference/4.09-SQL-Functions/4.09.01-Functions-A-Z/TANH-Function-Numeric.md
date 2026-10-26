# 4.9.1.194 TANH Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 349–350

Returns the hyperbolic tangent of the specified numeric argument.

## Syntax

```sql
TANH(<number>)
```

## Description

Returns the hyperbolic tangent of the numeric argument `<number>`.

## Example

The following example returns the value `0.7615941559557649` for `"tanh"`:

```sql
SELECT TANH (1.0) "tanh" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
