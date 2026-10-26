# 4.9.1.105 LAST_DAY Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 227

Returns the date of the last day of the month that contains the specified date.

## Syntax

```sql
LAST_DAY(<date>)
```

## Description

Returns the date of the last day of the month that contains the date `<date>`.

## Example

The following example returns the value `2010-01-31` (or another format like `Jan 31, 2010`, depending on your date display settings):

```sql
SELECT LAST_DAY (TO_DATE('2010-01-04', 'YYYY-MM-DD')) "last day" FROM DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
