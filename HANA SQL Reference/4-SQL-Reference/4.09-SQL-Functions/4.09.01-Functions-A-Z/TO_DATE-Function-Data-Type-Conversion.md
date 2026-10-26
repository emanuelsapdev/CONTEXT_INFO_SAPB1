# 4.9.1.201 TO_DATE Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 355

Converts a date string into a DATE data type.

## Syntax

```sql
TO_DATE(<date> [, <format>])
```

## Description

Converts the date string `<date>` into a DATE data type.

If the `<format>` specifier is omitted, the conversion is performed using the date format model.

## Example

The following example converts the string `2010-01-12` to a DATE value with the format `YYYY-MM-DD`, and returns the value `2010-01-12` (or another format like `Jan 12, 2010`, depending on your date display settings):

```sql
SELECT TO_DATE('2010-01-12', 'YYYY-MM-DD') "to date" FROM DUMMY;
```

## Related Information

[Data Type Conversion](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
