# 4.9.1.222 UMINUS Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 373–374

Returns the negated value of the specified numeric argument.

## Syntax

```sql
UMINUS(<number>)
```

## Description

Returns the negated value of the specified numeric argument.

## Example

The following example returns the value `765` for "uminus":

```sql
SELECT UMINUS(-765) "uminus" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
