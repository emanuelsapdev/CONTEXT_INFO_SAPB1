# 4.9.1.7 ADD_DAYS Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 89–90

Computes the specified date, plus or minus the specified number of days.

## Syntax

```sql
ADD_DAYS(<date>, <num_days>)
```

## Syntax Elements

**date** Specifies the date to increment. **num_days** Specifies the number of days (integer). A positive integer increments the date by the specified amount; a negative integer decrements the date.

## Description

Computes the specified date plus or minus the specified number of days.

## Example

The following example increments the date value `2009-12-05` by 30 days and returns the value `2010-01-04`:

```sql
SELECT ADD_DAYS (TO_DATE ('2009-12-05', 'YYYY-MM-DD'), 30) "add days" FROM DUMMY;
```

The following example decrements the date value `2009-12-05` by 30 days and returns the value `2009-11-05`:

```sql
SELECT ADD_DAYS (TO_DATE ('2009-12-05', 'YYYY-MM-DD'), -30) "subtract days" FROM
DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
