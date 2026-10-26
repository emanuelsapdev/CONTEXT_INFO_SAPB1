# 4.9.1.31 BITXOR Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 119–120

Performs an XOR operation on the bits of two arguments.

## Syntax

```sql
BITXOR(<expression1>, <expression2>)
```

## Syntax Elements

**expression1** An argument that must be a non-negative INTEGER or VARBINARY value. **expression2** An argument for the bitwise OR operation that must be a non-negative INTEGER or VARBINARY value.

## Description

Performs an XOR operation on the bits of the arguments `<expression1>` and `<expression2>`.

The BITXOR functions works a bit differently than the BITAND function. The BITAND function converts string arguments into BIGINT, whereas the BITXOR function converts string arguments into INT.

The BITXOR function returns a result along the argument's type.

## Example

The following example performs a bitwise XOR operation for the arguments `255` and `123`, and returns the value `132` for `"bitxor"`:

```sql
SELECT BITXOR (255, 123) "bitxor" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
