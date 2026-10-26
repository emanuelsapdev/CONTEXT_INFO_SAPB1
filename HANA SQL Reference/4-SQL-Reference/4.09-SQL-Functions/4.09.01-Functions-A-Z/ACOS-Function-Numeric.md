# 4.9.1.6 ACOS Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 88–89

Returns the arc-cosine, in radians, of a numeric argument between -1 and 1.

## Syntax

```sql
ACOS(<num>)
```

## Syntax Elements

**num** Specifies a numeric argument between -1 and 1.

## Description

Returns the arc-cosine, in radians, of the numeric argument `<n>` between -1 and 1.

## Example

The following example returns the value `1.0471975511965979`:

```sql
SELECT ACOS (0.5) "acos" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
