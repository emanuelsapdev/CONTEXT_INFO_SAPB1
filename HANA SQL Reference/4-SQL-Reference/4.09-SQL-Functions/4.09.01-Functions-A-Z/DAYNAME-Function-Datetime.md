# 4.9.1.67 DAYNAME Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 174–175

Returns the weekday name for the specified date.

## Syntax

```sql
DAYNAME(<date>)
```

## Description

Returns the weekday in English for the specified date.

## Example

The following example returns `Monday` as the weekday for the specified date:

```sql
SELECT DAYNAME ('2011-05-30') "dayname" FROM DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
