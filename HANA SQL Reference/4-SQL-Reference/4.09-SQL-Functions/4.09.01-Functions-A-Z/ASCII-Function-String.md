# 4.9.1.15 ASCII Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 100–101

Returns the integer ASCII value of the first character in a specified string.

## Syntax

```sql
ASCII(<string>)
```

## Syntax Elements

**string** Specifies the string to return the integer ASCII value from.

## Description

Returns the integer ASCII value of the first character in a string `<string>`.

## Example

This example converts the first character of the string `Ant` into a numeric ASCII value and returns the value `65`:

```sql
SELECT ASCII('Ant') "ascii" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
