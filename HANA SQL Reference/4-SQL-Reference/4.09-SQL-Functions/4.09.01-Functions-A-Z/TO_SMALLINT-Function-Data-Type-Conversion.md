# 4.9.1.214 TO_SMALLINT Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 366

Converts a value to a SMALLINT data type.

## Syntax

```sql
TO_SMALLINT(<value>)
```

## Description

If the input `<value>` has a mantissa, then these digits are truncated during the conversion process.

## Examples

The following example converts the value `10` to a SMALLINT and returns the value `10`:

```sql
SELECT TO_SMALLINT ('10') "to smallint" FROM DUMMY;
```

The following example converts the value `10` to a SMALLINT and returns the value `10`, truncating the mantissa:

```sql
SELECT TO_SMALLINT(10.5) "to int" FROM DUMMY;
```

## Related Information

[Data Type Conversion](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
