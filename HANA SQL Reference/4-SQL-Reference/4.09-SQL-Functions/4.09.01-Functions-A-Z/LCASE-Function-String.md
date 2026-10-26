# 4.9.1.107 LCASE Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 229–230

Converts all characters in a string to lowercase.

## Syntax

```sql
LCASE(<string>)
```

## Description

Converts all characters in string `<string>` to lowercase.

The LCASE function is identical to the LOWER function.

## Example

This example converts all characters of the given string `TesT` to lowercase and returns the value `test`.

```sql
SELECT LCASE ('TesT') "lcase" FROM DUMMY;
```

## Related Information

LOWER Function (String) [→](LOWER-Function-String.md) Character String Data Types [→](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
