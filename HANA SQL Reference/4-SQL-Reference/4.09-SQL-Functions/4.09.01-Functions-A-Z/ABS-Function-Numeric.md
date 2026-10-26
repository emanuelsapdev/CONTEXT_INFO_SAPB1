# 4.9.1.5 ABS Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 87–88

Returns the absolute value of a numeric argument.

## Syntax

```sql
ABS(<num>)
```

## Syntax Elements

**num** Specifies the numeric argument.

## Description

Returns the absolute value of the numeric argument `<num>`.

## Example

The following example returns the value `1` for `"absolute"`:

```sql
SELECT ABS (-1) "absolute" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
