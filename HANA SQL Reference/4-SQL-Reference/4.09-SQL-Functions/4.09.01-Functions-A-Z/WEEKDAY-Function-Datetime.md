# 4.9.1.230 WEEKDAY Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 381–382

Returns the day of the week for the specified date.

## Syntax

```sql
WEEKDAY(<date>)
```

## Description

Returns an integer representation of the day of the week for date `<date>`. The return value ranges from 0 to 6, representing Monday(0) through to Sunday(6).

## Example

The following example returns the value `4` as the weekday of the specified date:

```sql
SELECT WEEKDAY (TO_DATE ('2010-12-31', 'YYYY-MM-DD')) "week day" FROM DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
