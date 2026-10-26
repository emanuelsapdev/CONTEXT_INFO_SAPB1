# 4.9.1.37 CONCAT Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 125–126

Returns a combined string consisting of two specified strings.

## Syntax

```sql
CONCAT(<string1>, <string2>)
```

## Syntax Elements

**string1** Specifies the first string to combine. **string2** Specifies the second string to combine.

## Description

Returns a combined string consisting of `<string1>` followed by `<string2>`. The concatenation operator (||) is identical to this function.

The maximum length of the concatenated string is 8,388,607. If the string length is longer than the maximum length, an exception is thrown. Exceptionally, an implicit truncation is performed when converting an (N)CLOB typed value with a size greater than the maximum length of an (N)VARCHAR typed value.

If one ore both arguments are NULL, the function returns NULL.

## Example

This example concatenates the specified string arguments and returns the value `Cat`:

```sql
SELECT CONCAT ('C', 'at') "concat" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
