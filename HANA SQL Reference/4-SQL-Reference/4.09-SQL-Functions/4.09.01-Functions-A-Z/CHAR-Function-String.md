# 4.9.1.35 CHAR Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 123–124

Returns the character that has the ASCII value of the specified number.

## Syntax

```sql
CHAR(<number>)
```

## Syntax Elements

**number** Specifies the number with the ASCII value that the function converts into a character.

## Description

Returns the character that has the ASCII value of the specified number.

## Example

This example converts three ASCII values into characters and concatenates the results, returning the string `Ant`:

```sql
SELECT CHAR (65) || CHAR (110) || CHAR (116) "character" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
