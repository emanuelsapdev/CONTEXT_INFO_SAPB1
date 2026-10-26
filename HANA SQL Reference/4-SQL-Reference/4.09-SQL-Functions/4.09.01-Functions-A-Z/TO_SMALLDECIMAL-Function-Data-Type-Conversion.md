# 4.9.1.213 TO_SMALLDECIMAL Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 365–366

Converts the specified value to a SMALLDECIMAL data type.

## Syntax

```sql
TO_SMALLDECIMAL(<value>)
```

## Description

Converts the specified value to a SMALLDECIMAL data type.

## Example

The following example converts the value `7654321.89` to the SMALLDECIMAL value `7,654,321.89`:

```sql
SELECT TO_SMALLDECIMAL(7654321.89) "to smalldecimal" FROM DUMMY;
```

## Related Information

[Data Type Conversion](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
