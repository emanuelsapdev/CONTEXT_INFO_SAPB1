# 4.9.1.221 UCASE Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 372–373

Converts all characters in the specified string to uppercase.

## Syntax

```sql
UCASE(<string>)
```

## Description

Converts all characters in string `<string>` to uppercase.

The UCASE function is identical to the UPPER function.

## Example

The following example converts the given string to uppercase, and returns the value `ANT`:

```sql
SELECT UCASE ('Ant') "ucase" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
