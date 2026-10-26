# 4.9.1.90 HEXTOBIN Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 200–201

Converts a string of hexadecimal characters to a VARBINARY value.

## Syntax

```sql
HEXTOBIN(<hexadecimal_string>)
```

## Description

HEXTOBIN returns a VARBINARY value where each byte of the result corresponds to two characters of `<hexadecimal_string>`. If `<hexadecimal_string>` does not contain an even number of digits, an error is returned.

In SAP HANA, lowercase characters in `<hexadecimal_string>` are supported and are treated as uppercase.

## Example

The following two examples return the VARBINARY value `608DA975`:

```sql
SELECT HEXTOBIN ('608da975') "Result" FROM DUMMY;
```

```sql
SELECT HEXTOBIN ('608DA975') "Result" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
