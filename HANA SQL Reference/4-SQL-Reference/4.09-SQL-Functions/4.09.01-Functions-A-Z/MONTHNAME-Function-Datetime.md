# 4.9.1.130 MONTHNAME Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 259–260

Returns the name of the month for the specified date.

## Syntax

```sql
MONTHNAME(<date>)
```

## Description

Returns the name of the month for date `<date>`.

## Example

The following example returns the value `MAY`, the month name of the specified date:

```sql
SELECT MONTHNAME ('2011-05-30') "monthname" FROM DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
