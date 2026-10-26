# 4.9.1.149 QUARTER Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 281–282

Returns the quarter for the specified date.

## Syntax

```sql
QUARTER(<date>, [, <start_month> ])
```

## Description

Returns the numerical year and quarter of date `<date>`. The first quarter starts in the month specified by `<start_month>`. If `<start_month>` is not specified, then the first quarter is assumed to begin in January.

## Example

The following example returns the value `2011-Q4` as the year and quarter for the specified date:

```sql
SELECT QUARTER (TO_DATE('2012-01-01', 'YYYY-MM-DD'), 2) "quarter" FROM DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
