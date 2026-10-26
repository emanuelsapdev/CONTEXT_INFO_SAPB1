# 4.9.1.219 TRIM Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 370–371

Returns a string after removing leading and trailing spaces.

## Syntax

```sql
TRIM([[LEADING | TRAILING | BOTH] <trim_char> FROM] <string> )
```

## Syntax Elements

#### trim_char

Specifies the characters to be removed from a string.

## Description

Returns string `<string>` after removing leading and trailing spaces. The trimming operation is carried out either from the start (`LEADING`), end (`TRAILING`) or both (`BOTH`) ends of the string.

- If either `<string>` or `<trim_char>` are NULL values, then `NULL` is returned.
- If no options are specified, `TRIM` removes both the leading and trailing substring `<trim_char>` from string `<string>`.
- If `<trim_char>` is not specified, then a single blank space is used.

## Example

The following example removes the character `a` both at the beginning and at the end of the specified string, and returns the value `123456789`:

```sql
SELECT TRIM ('a' FROM 'aaa123456789aa') "trim both" FROM DUMMY;
```

The following example removes the character `a` at the begin of the specified string, and returns the value `123456789aa`:

```sql
SELECT TRIM (LEADING 'a' FROM 'aaa123456789aa') "trim leading" FROM DUMMY;
```
