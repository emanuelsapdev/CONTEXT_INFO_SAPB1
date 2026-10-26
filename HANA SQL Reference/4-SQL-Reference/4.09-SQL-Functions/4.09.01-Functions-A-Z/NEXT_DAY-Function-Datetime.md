# 4.9.1.135 NEXT_DAY Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 263–264

Returns the date of the day following the specified date.

## Syntax

```sql
NEXT_DAY(<date>)
```

## Description

Returns the date of the day following the specified date.

## Example

The following example returns `2010-01-01` as the day after `2009-12-31`:

```sql
SELECT NEXT_DAY (TO_DATE ('2009-12-31', 'YYYY-MM-DD')) "next day" FROM DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
