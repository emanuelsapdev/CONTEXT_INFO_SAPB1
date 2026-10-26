# 4.9.1.34 CEIL Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 122–123

Returns the first integer that is greater than or equal to the specified value.

## Syntax

```sql
CEIL(<number>)
```

## Syntax Elements

**number** Specifies the number that the function returns the integer for.

## Description

Returns the first integer that is greater than or equal to the value of `<n>`.

## Example

The following example returns the value `15` for `"ceiling"`:

```sql
SELECT CEIL (14.5) "ceiling" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
