# 4.9.1.223 UNICODE Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 374

Returns an integer containing the Unicode code point of the first character in the specified string.

## Syntax

```sql
UNICODE(<character>)
```

## Description

Returns an integer containing the Unicode code point of the first character in the string `<character>`, or `NULL` if the first character is not a valid encoding.

## Example

The following example returns the Unicode code point for the given character (`35`):

```sql
SELECT UNICODE ('#') "unicode" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
