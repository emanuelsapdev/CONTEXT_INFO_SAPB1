# 4.9.1.113 LN Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 238

Returns the natural logarithm of a number.

## Syntax

```sql
LN(<number>)
```

## Description

Returns the natural logarithm of the specified number.

## Example

This example returns the natural logarithm of the number `9`, which is `2.1972245773362196`:

```sql
SELECT LN (9) "ln" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
