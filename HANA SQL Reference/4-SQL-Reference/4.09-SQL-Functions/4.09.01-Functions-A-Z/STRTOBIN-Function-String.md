# 4.9.1.185 STRTOBIN Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 339

Converts all characters in a string into a binary encoding using the specified codepage.

## Syntax

```sql
STRTOBIN(<string>, <codepage>)
```

## Description

Converts all characters in string `<string>` into a binary encoding using the defined `<codepage>`.

## Example

This example converts all characters in the given string to binary `UTF-16BE` encoding, and returns the value `0041006E0074`:

```sql
SELECT STRTOBIN ('Ant', 'UTF-16BE') "strtobin" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
