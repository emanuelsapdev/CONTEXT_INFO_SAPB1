# 4.9.1.160 RIGHT Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 296–297

Returns the specified number of characters/bytes of a string, starting from the right side.

## Syntax

```sql
RIGHT(<string>, <number>)
```

## Syntax Elements

#### string

Specifies the string to be operated on.

#### number

Specifies the length of characters or bytes to return, starting from the right side.

## Description

Returns the rightmost `<number>` characters/bytes of string `<string>`.

Returns an empty string value if `<number>` is less than 1.

Returns string specified by `<string>` (without blank padding) if the value of `<number>` is greater than the length of string specified by `<string>`.

## Example

The following example returns the rightmost `3` characters of the given string (`789`):

```sql
SELECT RIGHT('HI0123456789', 3) "right" FROM DUMMY;
```

The following example returns the entire input string because the value `20` exceeds the length of the input string:

```sql
SELECT RIGHT('HI0123456789', 20) "right" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
