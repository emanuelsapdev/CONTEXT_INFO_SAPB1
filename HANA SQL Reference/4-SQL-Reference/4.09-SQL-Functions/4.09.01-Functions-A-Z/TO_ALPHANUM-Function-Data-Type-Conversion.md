# 4.9.1.195 TO_ALPHANUM Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 350

Converts a given value to an ALPHANUM data type.

## Syntax

```sql
TO_ALPHANUM(<value>)
```

## Description

Converts a given `<value>` to an ALPHANUM data type.

## Example

The following example converts the value `10` to the ALPHANUM value `10`.

```sql
SELECT TO_ALPHANUM ('10') "to alphanum" FROM DUMMY;
```

## Related Information

[Data Type Conversion](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
