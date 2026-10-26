# 4.9.1.217 TO_TINYINT Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 368–369

Converts a value to a TINYINT data type.

## Syntax

```sql
TO_TINYINT(<value>)
```

## Description

Converts the `<value>` to a TINYINT data type.

If the input value has a mantissa, then these digits are truncated during the conversion process.

## Examples

The following example converts the value `10` to the TINYINT value `10`:

```sql
SELECT TO_TINYINT ('10') "to tinyint" FROM DUMMY;
```

The following example converts the value `10.5` to the TINYINT value `10`, truncating the mantissa:

```sql
SELECT TO_TINYINT(10.5) "to tinyint" FROM DUMMY;
```

## Related Information

[Data Type Conversion](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
