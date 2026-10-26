# 4.9.1.162 RPAD Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 299–300

Right-pads a string with spaces or a specified pattern to make a string that is a specified number of characters in length.

## Syntax

```sql
RPAD(<string>, <number> [, <pattern>])
```

## Syntax Elements

#### string

Specifies the string to be padded.

#### number

Specifies the length to pad `<string>`. `<number>` must be an integer.

#### pattern

Specifies a string of characters, rather than spaces, to use for padding.

## Description

Right-pads the end of `<string>` with spaces or characters to make a string of `<number>` characters in length. If `<pattern>` is specified, then `<string>` is padded using sequences of the given characters until the required length is met.

If the length of `<string>` is greater than `<n>`, then no padding is performed and the resulting value is truncated to the length specified in `<number>`.

RPAD returns an empty string value if `<number>` is less than 1.

## Example

The following example right-pads the end of string `end` with the pattern `12345` to make a string of `15` characters in length and returns the value `end123451234512`:

```sql
SELECT RPAD ('end', 15, '12345') "right padded" FROM DUMMY;
```

In the following example, `<str>` is longer than `<n>`, so no padding is performed and the result is `<str>` truncated to the length of `<n>` (that is, `en`):

```sql
SELECT RPAD ('end', 2, '12345') "right padded" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
