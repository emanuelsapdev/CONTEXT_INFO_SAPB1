# 4.9.1.216 TO_TIMESTAMP Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 367–368

Converts a date string to a TIMESTAMP data type.

## Syntax

```sql
TO_TIMESTAMP(<date> [, <format>])
```

## Description

Converts date string `<date>` to the TIMESTAMP data type.

If the `<format>` specifier is omitted, then the conversion is performed using the date format model.

## Example

The following example converts the value `2010-01-11 13:30:00` to the TIMESTAMP value `2010-01-11 13:30:00.0` using the format `YYYY-MM-DD HH24:MI:SS`:

```sql
SELECT TO_TIMESTAMP ('2010-01-11 13:30:00', 'YYYY-MM-DD HH24:MI:SS') "to
timestamp" FROM DUMMY;
```

## Related Information

[Data Type Conversion](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
