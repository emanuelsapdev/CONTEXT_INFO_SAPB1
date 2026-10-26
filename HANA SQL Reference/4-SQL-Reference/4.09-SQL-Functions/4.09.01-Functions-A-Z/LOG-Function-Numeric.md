# 4.9.1.117 LOG Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 243–244

Returns the natural logarithm of a specified number and base.

## Syntax

```sql
LOG(<base>, <number>)
```

## Description

Returns the natural logarithm of a number specified by `<number>` and a base specified by `<base>`, where `<base>` must be a positive value other than 1, and `<number>` must be any positive value.

## Example

The following example returns the natural logarithm for 2 base 10, which is `0.30102999566398114`:

```sql
SELECT LOG (10, 2) "log" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
