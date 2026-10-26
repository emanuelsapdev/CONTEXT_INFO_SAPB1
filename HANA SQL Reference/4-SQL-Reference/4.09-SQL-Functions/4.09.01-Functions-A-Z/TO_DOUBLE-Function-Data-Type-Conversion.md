# 4.9.1.204 TO_DOUBLE Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 357–358

Converts a value to a DOUBLE data type.

## Syntax

```sql
TO_DOUBLE(<value>)
```

## Description

Converts a specified `<value>` to a DOUBLE (double precision) data type.

## Example

The following example converts 15.12 to a DOUBLE, and then multiplies the value by 3, returning the DOUBLE value 45.36.

```sql
SELECT 3*TO_DOUBLE ('15.12') "to double" FROM DUMMY;
```

## Related Information

[Data Type Conversion](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
