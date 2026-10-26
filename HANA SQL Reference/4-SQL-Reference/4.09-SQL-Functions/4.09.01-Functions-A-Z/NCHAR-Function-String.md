# 4.9.1.133 NCHAR Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 262–263

Returns the Unicode character with the specified code number.

## Syntax

```sql
NCHAR(<number>)
```

## Description

Returns the Unicode character with the specified code number `<number>`.

## Example

This example returns the Unicode character (`A`) with the code number `65`:

```sql
SELECT NCHAR (65) "nchar" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
