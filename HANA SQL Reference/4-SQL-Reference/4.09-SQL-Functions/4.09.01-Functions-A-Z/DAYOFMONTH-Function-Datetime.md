# 4.9.1.68 DAYOFMONTH Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 175–176

Returns the day of the month for the specified date.

## Syntax

```sql
DAYOFMONTH(<date>)
```

## Description

Returns an integer for the day of the month for the specified date.

## Example

The following example returns `30` as the number for the day of the month for the specified date:

```sql
SELECT DAYOFMONTH ('2011-05-30') "dayofmonth" FROM DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
