# 4.9.1.78 EXP Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 186–187

Returns the result of the base of the natural logarithms e raised to the power of the specified argument.

## Syntax

```sql
EXP(<number>)
```

## Description

Returns the result of the base of the natural logarithms e raised to the power of the argument `<number>`.

## Example

The following example returns the value `2.718281828459045` for `"exp"`:

```sql
SELECT EXP (1.0) "exp" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
