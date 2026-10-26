# 4.9.1.4 ABAP_UPPER Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 86–87

Converts all characters in the specified string to uppercase.

## Syntax

```sql
ABAP_UPPER(<string>)
```

## Syntax Elements

**string** The string to convert to uppercase.

## Description

Converts all characters in the `<string>` parameter to uppercase.

## Example

The following example converts the given string to uppercase and returns the value `ANT`:

```sql
SELECT ABAP_UPPER ('Ant') "uppercase" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
