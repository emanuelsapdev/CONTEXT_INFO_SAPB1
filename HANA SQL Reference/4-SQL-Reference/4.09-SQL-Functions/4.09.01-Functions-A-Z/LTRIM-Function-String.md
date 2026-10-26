# 4.9.1.120 LTRIM Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 246–247

Returns a string, trimmed of all leading spaces.

## Syntax

```sql
LTRIM(<string> [, <remove_set>])
```

## Description

Returns string `<string>`, trimmed of all leading spaces. If `<remove_set>` is specified, LTRIM removes all the characters contained in this set from the start of string `<string>`. This process continues until a character that is not in `<remove_set>` is reached.

`<remove_set>` is treated as a set of characters and not as a search string.

## Example

This example removes all leading `a` and `b` characters from the given string and returns the value Aabend:

```sql
SELECT LTRIM ('babababAabend','ab') "ltrim" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
