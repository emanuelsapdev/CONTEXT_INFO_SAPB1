# 4.9.1.8 ADD_MONTHS Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 90–91

Computes the specified date plus the specified number of months.

## Syntax

```sql
ADD_MONTHS(<date>, <num_months>)
```

## Syntax Elements

**date** The date that is incremented. **num_months** The number of months by which to increment the date.

## Description

Computes the specified date plus the specified number of months.

To compute the date so that the output date is set to the last day of the month when the input date is the last day of the month, use the ADD_MONTHS_LAST function.

The parameter `<date>` must be implicitly or explicitly converted to one of the following SQL data types:

- DATE
- TIMESTAMP
- SECONDDATE

The SQL data type of the output parameters is the same as the SQL data type of the input parameters. For example, ADD_MONTHS_LAST(DATE) returns a date, while ADD_MONTHS_LAST(TIMESTAMP) returns a timestamp.

## Example

The following example increments the date 2009-12-05 by one month, and returns the value 2010-01-05:

```sql
SELECT ADD_MONTHS (TO_DATE ('2009-12-05', 'YYYY-MM-DD'), 1) "add months" FROM
DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
