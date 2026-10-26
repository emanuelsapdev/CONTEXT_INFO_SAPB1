# 4.9.1.206 TO_INT Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 359–360

Converts a value to an INT data type.

## Syntax

```sql
TO_INT(<value>)
```

## Description

If the input `<value>` has a mantissa, then the mantissa is truncated during the conversion process.

## Examples

The following example converts the value `10` to the INT value `10`:

```sql
SELECT TO_INT('10') "to int" FROM DUMMY;
```

The following example converts the value `10.5` to the INT value `10`, truncating the mantissa:

```sql
SELECT TO_INT(10.5) "to int" FROM DUMMY;
```

## Related Information

[Data Type Conversion](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
