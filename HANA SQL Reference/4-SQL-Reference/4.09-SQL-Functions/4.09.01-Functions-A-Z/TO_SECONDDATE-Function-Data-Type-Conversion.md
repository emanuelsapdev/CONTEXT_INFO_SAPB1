# 4.9.1.212 TO_SECONDDATE Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 364–365

Converts a specified date string to a SECONDDATE data type.

## Syntax

```sql
TO_SECONDDATE(<date> [, <format>])
```

## Description

If the `<format>` specifier is omitted, then the conversion is performed using the date format model.

## Example

The following example converts the value `2010-01-11 13:30:00` to a SECONDDATE data type with format `YYYY-MM-DD HH24:MI:SS` and returns the value `2010-01-11 13:30:00.0` (or another format like `Jan 11, 2010 1:30:00.0 PM`, depending on your date display settings):

```sql
SELECT TO_SECONDDATE ('2010-01-11 13:30:00', 'YYYY-MM-DD HH24:MI:SS') "to
seconddate" FROM DUMMY;
```

## Related Information

[Data Type Conversion](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
