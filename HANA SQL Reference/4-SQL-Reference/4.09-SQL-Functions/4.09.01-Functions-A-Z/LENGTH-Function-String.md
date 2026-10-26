# 4.9.1.111 LENGTH Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 233–234

Returns the number of characters in a string.

## Syntax

```sql
LENGTH(<string>)
```

## Description

Returns the number of characters in string `<string>`.

If `<string>` is a `VARCHAR`, then the function does not return the number of bytes. In this case, the number of characters like `NVARCHAR`-typed strings are returned instead.

Supplementary plane Unicode characters, each of which occupies 6 bytes in CESU-8 encoding, are counted as two characters.

## Example

This example returns the number of characters (`14`) contained in the given string:

```sql
SELECT LENGTH ('length in char') "length" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
