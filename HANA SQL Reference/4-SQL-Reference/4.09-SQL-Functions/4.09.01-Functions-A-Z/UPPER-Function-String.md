# 4.9.1.224 UPPER Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 374–375

Converts all characters in a string to uppercase.

## Syntax

```sql
UPPER(<string>)
```

## Description

Converts all characters in string `<string>` to uppercase.

The UPPER function is identical to the UCASE function.

## Example

This example converts the given string `Ant` to uppercase and returns the value `ANT`:

```sql
SELECT UPPER ('Ant') "uppercase" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
