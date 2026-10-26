# 4.9.1.16 ASIN Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 101–102

Returns the arc-sine, in radians, of a numeric argument.

## Syntax

```sql
ASIN(<number>)
```

## Syntax Elements

**number** Specifies a numeric argument between -1 and 1.

## Description

Returns the arc-sine, in radians, of the numeric argument `<number>` between -1 and 1.

## Example

The following example returns the value `0.5235987755982989` for `"asin"`:

```sql
SELECT ASIN (0.5) "asin" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
