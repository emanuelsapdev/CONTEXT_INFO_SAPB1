# 4.9.1.197 TO_BINARY Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 351–352

Converts a value to a BINARY data type.

## Syntax

```sql
TO_BINARY(<value>)
```

## Description

Converts a `<value>` to a BINARY data type.

## Example

The following example converts the value `abc` to the BINARY value `616263`.

```sql
SELECT TO_BINARY ('abc') "to binary" FROM DUMMY;
```

## Related Information

[Data Type Conversion](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
