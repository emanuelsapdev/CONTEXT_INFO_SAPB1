# 4.9.1.18 ATAN2 Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 103–104

Returns the arc-tangent, in radians, of the ratio of two numbers.

## Syntax

```sql
ATAN2(<number1>, <number2>)
```

## Syntax Elements

**number1** Specifies the first numeric argument. **number2** Specifies the second numeric argument.

## Description

Returns the arc-tangent, in radians, of the ratio of two numbers `<number1>` and `<number2>`.

## Example

The following example returns the value `0.4636476090008061` for `"atan2"`:

```sql
SELECT ATAN2 (1.0, 2.0) "atan2" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
