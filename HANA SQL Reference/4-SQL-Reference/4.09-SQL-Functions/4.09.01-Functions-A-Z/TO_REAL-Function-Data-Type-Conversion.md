# 4.9.1.211 TO_REAL Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 363–364

Converts a `<value>` to a REAL data type.

## Syntax

```sql
TO_REAL(<value>)
```

## Description

Converts a `<value>` to a REAL (single precision) data type.

## Example

The following example converts the value `15.12` to a REAL value and multiplies it by `3` to return the value `45.36000061035156`.

```sql
SELECT 3*TO_REAL ('15.12') "to real" FROM DUMMY;
```

## Related Information

[Data Type Conversion](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
