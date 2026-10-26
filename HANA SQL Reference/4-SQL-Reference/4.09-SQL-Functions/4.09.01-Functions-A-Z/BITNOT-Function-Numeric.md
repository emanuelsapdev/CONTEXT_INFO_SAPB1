# 4.9.1.27 BITNOT Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 115–116

Performs a bitwise NOT operation on the bits of an expression.

## Syntax

```sql
BITNOT(<expression>)
```

## Syntax Elements

**expression** Specifies the expression that the function performs a bitwise NOT operation on. `<expression>` must be an INTEGER value.

## Description

Performs a bitwise NOT operation on the bits of the argument `<expression>`.

The BITNOT functions works a bit differently than the BITAND function. The BITAND function converts string arguments into BIGINT, whereas the BITNOT function converts string arguments into INT.

The BITNOT function returns a result along the argument's type.

## Example

The following example performs a BITNOT operation on `255`, and returns the value `-256` for `"bitnot"`:

```sql
SELECT BITNOT (255) "bitnot" FROM DUMMY;
```

## Related Information

Expressions [→](../../4.06-Expressions.md) Numeric Data Types [→](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
