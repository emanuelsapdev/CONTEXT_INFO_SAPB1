# 4.9.1.207 TO_INTEGER Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 360

Converts the `<value>` to an INTEGER data type.

## Syntax

```sql
TO_INTEGER(<value>)
```

## Description

If the input `<value>` has a mantissa, then these digits are truncated during the conversion process.

## Examples

The following example converts the value `10` to the INTEGER value `10`:

```sql
SELECT TO_INTEGER ('10') "to int" FROM DUMMY;
```

The following example converts the value `10.5` to the INTEGER value `10`, truncating the mantissa:

```sql
SELECT TO_INTEGER(10.5) "to int" FROM DUMMY;
```

## Related Information

[Data Type Conversion](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
