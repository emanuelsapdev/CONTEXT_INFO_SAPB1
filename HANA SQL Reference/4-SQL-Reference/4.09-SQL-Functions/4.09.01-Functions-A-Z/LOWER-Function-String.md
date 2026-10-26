# 4.9.1.118 LOWER Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 244–245

Converts all characters in a string to lowercase.

## Syntax

```sql
LOWER(<string>)
```

## Description

Converts all characters in `<string>` to lowercase.

The LOWER function is identical to the LCASE function.

## Example

This example converts the given string `AnT` to lowercase, and returns the value `ant`:

```sql
SELECT LOWER ('AnT') "lower" FROM DUMMY;
```

## Related Information

LCASE Function (String) [→](LCASE-Function-String.md) Character String Data Types [→](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
