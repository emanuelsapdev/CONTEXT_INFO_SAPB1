# 4.9.1.148 POWER Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 281

Calculates a specified base number raised to the power of a specified exponent.

## Syntax

```sql
POWER(<base>, <exponent>)
```

## Description

Calculates a specified base number raised to the power of a specified exponent.

## Example

The following example returns the value `1024`:

```sql
SELECT POWER (2, 10) "power" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
