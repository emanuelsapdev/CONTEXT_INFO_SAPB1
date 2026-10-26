# 4.9.1.110 LEFT Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 232–233

Returns the specified number of characters or bytes of a string, starting from the left side.

## Syntax

```sql
LEFT(<string>, <number>)
```

## Syntax Elements

#### string

Specifies the string to be operated on.

#### number

Specifies the length of characters or bytes to return, starting from the left side.

## Description

Returns the first `<number>` of characters or bytes from the beginning of `<string>`.

Returns an empty string value if `<number>` is less than 1.

Returns `<string>` (without blank padding) if the value of `<number>` is greater than the length of `<string>`.

## Example

The following example returns the leftmost three characters of the string `Hel`:

```sql
SELECT LEFT ('Hello', 3) "left" FROM DUMMY;
```

The following example returns the string `Hello` because the value 10 exceeds the string length:

```sql
SELECT LEFT ('Hello', 10) "left" FROM DUMMY;
```
