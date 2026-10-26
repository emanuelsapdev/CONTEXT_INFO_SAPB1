# 4.9.1.163 RTRIM Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 300–301

Returns a string trimmed of all trailing spaces.

## Syntax

```sql
RTRIM(<string> [,<remove_set> ])
```

## Description

Returns a string trimmed of all trailing spaces. If `<remove_set>` is specified, then `RTRIM` removes all the characters contained in the specified set from the end of the string. This process continues until a character that is not in the `<remove_set>` has been reached.

`<remove_set>` is treated as a set of characters and not as a search string.

## Example

This example removes all trailing `a` and `b` characters from the given string, and returns the value `endabA`:

```sql
SELECT RTRIM ('endabAabbabab','ab') "rtrim" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
