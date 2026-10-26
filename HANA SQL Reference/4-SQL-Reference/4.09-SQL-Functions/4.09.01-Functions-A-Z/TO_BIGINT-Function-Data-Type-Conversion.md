# 4.9.1.196 TO_BIGINT Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 350–351

Converts a value to a BIGINT data type.

## Syntax

```sql
TO_BIGINT(<value>)
```

## Description

If the input `<value>` has a mantissa, then these digits are truncated during the conversion process.

## Examples

The following example converts the value `10` to a BIGINT value `10`:

```sql
SELECT TO_BIGINT ('10') "to bigint" FROM DUMMY;
```

The following example converts the value `10.5` to a BIGINT value `10`, truncating the mantissa:

```sql
SELECT TO_BIGINT (10.5) "to bigint" FROM DUMMY;
```

## Related Information

[Data Type Conversion](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
