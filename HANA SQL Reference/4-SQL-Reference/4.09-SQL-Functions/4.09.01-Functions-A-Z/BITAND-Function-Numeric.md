# 4.9.1.25 BITAND Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 113–114

Performs an AND operation on the bits of two arguments.

## Syntax

```sql
BITAND(<value1>, <value2>)
```

## Syntax Elements

**value1** The argument must be non-negative INTEGER or VARBINARY value. **value2** The argument must be non-negative INTEGER or VARBINARY value.

## Description

Performs an AND operation on the bits of the arguments `<value1>` and `<value2>`.

The BITAND function works a bit differently from the BITOR, BITXOR, and BITNOT functions. The BITAND function converts string arguments into BIGINT, whereas the other functions convert string arguments into INT.

The BITAND function returns a result along the argument's type.

## Example

The following example returns the value `123`:

```sql
SELECT BITAND (255, 123) "bitand" FROM DUMMY;
```

## Related Information

Expressions [→](../../4.06-Expressions.md) Numeric Data Types [→](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
