# 4.9.1.13 ADD_YEARS Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 98–99

Computes the specified date plus the specified years.

## Syntax

```sql
ADD_YEARS(<date>, <num_years>)
```

## Syntax Elements

**date** The date that is incremented. **num_years** The number of years by which to increment the date.

## Description

Computes the specified date plus the specified number of years.

## Example

The following example increments the specified date value `2009-12-05` by `1` year, and returns the value `2010-12-05`:

```sql
SELECT ADD_YEARS (TO_DATE ('2009-12-05', 'YYYY-MM-DD'), 1) "add years" FROM
DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
