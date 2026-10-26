# 4.9.1.1 ABAP_ALPHANUM Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 82–84

Converts a string to what would result if the string was transformed into an ALPHANUM type and then converted back to a string.

## Syntax

```sql
ABAP_ALPHANUM( <string>, <chars> )
```

## Syntax Elements

**string** Specifies the input string to convert. **chars** Specifies the length to left-pad `<string>` with (using 0s) if `<string>` is shorter than the length specified by `<chars>`.

## Description

The input value, `<string>`, is checked to find out if it is numeric or a mixture of numeric and non-numeric. If `<string>` is numeric, then it is left-padded with zeroes up to the length specified by `<chars>`, if necessary. If `<string>` is a mixture or numeric and non-numeric, or is empty, then it is returned unchanged.

Strings that start with spaces and contain only digits after the whitespace prefix are regarded as numeric.

## Example

The following example returns `012`. Since `<chars>` is set to 3, the left-most digit is padded with a 0.

```sql
SELECT ABAP_ALPHANUM('12', 3) FROM DUMMY;
```

The following example returns `1234`. The input value was numeric and was not shorter than `<chars>`, so no left-padding was required.

```sql
SELECT ABAP_ALPHANUM('1234', 3) FROM DUMMY;
```

The following example returns `12x`. Because the input value contained a mixture of numeric and non-numeric, it is returned unchanged.

```sql
SELECT ABAP_ALPHANUM('12x', 13) FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
