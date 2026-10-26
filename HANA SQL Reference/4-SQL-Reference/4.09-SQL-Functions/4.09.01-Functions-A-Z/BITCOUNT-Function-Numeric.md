# 4.9.1.26 BITCOUNT Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 114–115

Counts the number of set bits of an expression.

## Syntax

```sql
BITCOUNT(<expression>)
```

## Syntax Elements

**expression** Specifies the expression that the function counts the number of set bits of. `<expression>` must be an INTEGER or a VARBINARY value.

## Description

Counts the number of set bits of the argument `<expression>`.

The BITCOUNT function returns an INTEGER value.

## Example

The following example counts the bits for `255`, and returns the value `8`:

```sql
SELECT BITCOUNT (255) "bitcount" FROM DUMMY;
```

## Related Information

Expressions [→](../../4.06-Expressions.md) Numeric Data Types [→](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
