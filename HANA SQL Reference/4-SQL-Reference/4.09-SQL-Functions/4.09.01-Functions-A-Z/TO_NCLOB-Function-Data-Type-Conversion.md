# 4.9.1.209 TO_NCLOB Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 361–362

Converts a `<value>` to an NCLOB data type.

## Syntax

```sql
TO_NCLOB(<value>)
```

## Description

Converts a `<value>` to an NCLOB data type.

## Example

The following example converts the value `TO_NCLOB converts the value to a NCLOB data type` to an NCLOB value.

```sql
SELECT TO_NCLOB ('TO_NCLOB converts the value to a NCLOB data type') "to nclob"
FROM DUMMY;
```

## Related Information

[Data Type Conversion](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
