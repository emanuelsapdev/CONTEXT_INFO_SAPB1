# 4.9.1.237 YEAR Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 398–399

Returns the year number of a specified date.

## Syntax

```sql
YEAR(<date>)
```

## Description

Returns the year number of date `<date>`.

## Example

The following example returns the value `2011` for the year of the specified date:

```sql
SELECT YEAR (TO_DATE ('2011-05-30', 'YYYY-MM-DD')) "year" FROM DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
