# 4.9.1.28 BITOR Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 116–117

This function performs an OR operation on the bits of two arguments.

## Syntax

```sql
BITOR(<expression1>, <expression2>)
```

## Syntax Elements

**expression1** An argument for the bitwise OR operation that must be a non-negative INTEGER or VARBINARY value. **expression2** An argument for the bitwise OR operation that must be a non-negative INTEGER or VARBINARY value.

## Description

This function performs an OR operation on the bits of the arguments `<expression1>` and `<expression2>`.

The BITOR functions works a bit differently than the BITAND function. The BITAND function converts string arguments into BIGINT, whereas the BITOR function converts string arguments into INT.

The BITOR function returns a result along the argument's type.

## Example

The following example performs a bitwise OR operation for the arguments `255` and `123`, and returns the value `255` for `"bitor"`:

```sql
SELECT BITOR (255, 123) "bitor" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
