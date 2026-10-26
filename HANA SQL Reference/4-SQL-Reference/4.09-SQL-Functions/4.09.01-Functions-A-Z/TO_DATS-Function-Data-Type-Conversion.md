# 4.9.1.202 TO_DATS Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 355–356

Converts a date string into an ABAP DATE string.

## Syntax

```sql
TO_DATS(<date>)
```

## Description

Converts the date string `<date>` into an ABAP DATE string with format 'YYYYMMDD'.

## Example

The following example converts the value `2010-01-12` to the ABAP DATE string`20100112`.

```sql
SELECT TO_DATS ('2010-01-12') "abap date" FROM DUMMY;
```

## Related Information

[Data Type Conversion](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
