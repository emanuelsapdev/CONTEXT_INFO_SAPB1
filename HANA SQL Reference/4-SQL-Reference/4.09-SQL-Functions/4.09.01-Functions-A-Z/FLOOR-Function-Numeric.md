# 4.9.1.82 FLOOR Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 190–191

Returns the largest integer that is not greater than the specified numeric argument.

## Syntax

```sql
FLOOR(<number>)
```

## Description

Returns the largest integer that is not greater than the numeric argument `<number>`.

## Example

The following example returns the value `14` for "floor":

```sql
SELECT FLOOR (14.5) "floor" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
