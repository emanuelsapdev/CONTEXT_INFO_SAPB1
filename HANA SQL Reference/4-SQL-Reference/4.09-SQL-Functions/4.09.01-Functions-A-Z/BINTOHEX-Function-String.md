# 4.9.1.22 BINTOHEX Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 110–111

Converts a binary string to a VARCHAR hexadecimal value.

## Syntax

```sql
BINTOHEX(<expression>)
```

## Syntax Elements

**expression** The value to be converted to a hexadecimal value.

## Description

Converts a binary value to a hexadecimal value as a VARCHAR data type. If the input value is not a binary value, then it is first converted to a binary value.

## Example

The following example converts the binary value `AB` to a hexadecimal VARCHAR value `4142`:

```sql
SELECT BINTOHEX('AB') "bintohex" FROM DUMMY;
```

## Related Information

Expressions [→](../../4.06-Expressions.md) Character String Data Types [→](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
