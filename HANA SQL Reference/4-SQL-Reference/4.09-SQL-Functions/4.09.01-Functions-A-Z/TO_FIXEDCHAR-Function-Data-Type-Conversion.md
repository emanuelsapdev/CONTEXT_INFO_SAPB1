# 4.9.1.205 TO_FIXEDCHAR Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 358–359

Converts a specified number of characters from a string starting at the first character in the string.

## Syntax

```sql
TO_FIXEDCHAR(<string>, <size>)
```

## Description

Converts the `<string>` to the specified `<size>`, starting at the first character. `<size>` cannot be a variable.

## Example

The following example converts the value `Ant` to a length of `2`, and returns the value `An`.

```sql
SELECT TO_FIXEDCHAR ('Ant', 2) "to_fixedchar" FROM DUMMY;
```

## Related Information

[Data Type Conversion](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
