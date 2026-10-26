# 4.9.1.119 LPAD Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 245–246

Left-pads a string with spaces, or a specified pattern, to make a string of a specified number of characters in length.

## Syntax

```sql
LPAD(<string>, <number> [, <pattern>])
```

## Syntax Elements

#### string

Specifies a string to be padded.

#### number

Specifies the length to which to pad `<string>`. `<number>` must be an integer.

#### pattern

Specifies a string of characters to use for padding instead of spaces.

## Description

Left-pads the end of `<string>` with spaces to make a string of `<number>` characters. If `<pattern>` is specified, then `<string>` is padded using sequences of the given characters until the required length is met.

If the length of `<string>` is greater than `<number>`, then no padding is performed and the resulting value is truncated from the right side to the length specified in `<number>`.

LPAD returns an empty string value if `<number>` is less than 1.

## Example

The following example left-pads the start of string `end` with the pattern `12345` to make a string of `15` characters in length, and returns the value `123451234512end`:

```sql
SELECT LPAD ('end', 15, '12345') "lpad" FROM DUMMY;
```

In the following example, `<string>` is longer than `<n>`, so no padding is performed and the result is `<string>` truncated to the length of `<number>` (that is, `en`):

```sql
SELECT LPAD ('end', 2, '12345') "lpad" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
