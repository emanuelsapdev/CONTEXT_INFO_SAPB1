# 4.9.1.199 TO_BOOLEAN Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 353–354

Converts a value to a BOOLEAN data type.

## Syntax

```sql
TO_BOOLEAN(<value>)
```

## Syntax Elements

**value** If `<value>` is:

- `1`, `'true'`, or `true` then TO_BOOLEAN returns the value `true`.
- `0`, `'false'`, or `false` then TO_BOOLEAN returns the value `false`.
- `unknown(Boolean)` or '`unknown`' then TO_BOOLEAN returns the value .

'`true`', '`false`', and '`unknown`' are not case sensitive, meaning that values of '`TRUE`' and '`TruE`' are treated the same as a value of `true`. TO_BOOLEAN throws an exception when `<value>` is not one of `true`, `false`, `unknown`, 0, 1, '0', '1', `'true'`, `'false'` or `'unknown'`.

## Description

Converts a `<value>` to a BOOLEAN data type.

## Example

Converts the value `0` to the BOOLEAN value `FALSE`.

```sql
SELECT TO_BOOLEAN(0) FROM DUMMY;
```

Converts the value `1` to the BOOLEAN value `TRUE`.

```sql
SELECT TO_BOOLEAN(1) FROM DUMMY;
```

## Related Information

[Boolean Data Type](../../4.03-Data-Types/4.03.02-Boolean-Data-Type.md)
