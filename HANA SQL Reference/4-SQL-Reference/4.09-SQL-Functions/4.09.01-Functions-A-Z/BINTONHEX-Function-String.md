# 4.9.1.23 BINTONHEX Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 111–112

Converts a binary value to a hexadecimal value as an NVARCHAR data type.

## Syntax

```sql
BINTONHEX(<expression>)
```

## Syntax Elements

**expression** The value to be converted to a hexadecimal value.

## Description

Converts a binary value to a hexadecimal value as an NVARCHAR data type. The input value is converted to a binary value first if it is not a binary value.

## Example

The following example converts the binary value `AB` to a hexadecimal NVARCHAR value `4142`.

```sql
SELECT BINTONHEX('AB') "bintonhex" FROM DUMMY;
```

## Related Information

Expressions [→](../../4.06-Expressions.md) Character String Data Types [→](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
