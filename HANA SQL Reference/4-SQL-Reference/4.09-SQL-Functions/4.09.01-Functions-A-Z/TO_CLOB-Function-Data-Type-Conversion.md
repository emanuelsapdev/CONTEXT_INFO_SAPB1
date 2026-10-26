# 4.9.1.200 TO_CLOB Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 354–355

Converts a value to a CLOB data type.

## Syntax

```sql
TO_CLOB(<value>)
```

## Description

Converts a `<value>` to a CLOB data type.

## Example

The following example converts the value `TO_CLOB converts the value to a CLOB data type` to a CLOB value.

```sql
SELECT TO_CLOB ('TO_CLOB converts the value to a CLOB data type') "to clob" FROM
DUMMY;
```

## Related Information

[Data Type Conversion](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
