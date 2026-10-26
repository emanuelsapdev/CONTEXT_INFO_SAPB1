# 4.9.1.3 ABAP_LOWER Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 85–86

Converts all characters in a specified string to lowercase.

## Syntax

```sql
ABAP_LOWER(<string>)
```

## Syntax Elements

**string** The string to convert to lowercase.

## Description

Converts all characters in the `<string>` parameter to lowercase.

## Example

The following example converts the given string to lowercase and returns the value `ant`:

```sql
SELECT ABAP_LOWER ('AnT') "lower" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
