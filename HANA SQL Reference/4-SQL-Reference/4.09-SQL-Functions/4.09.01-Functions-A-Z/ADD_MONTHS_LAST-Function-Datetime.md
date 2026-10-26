# 4.9.1.9 ADD_MONTHS_LAST Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 91–92

Computes the specified date plus the specified number of months, with the output date being the last day of the month if the input date is the last day of the month, even if those two dates differ.

## Syntax

```sql
ADD_MONTHS_LAST(<date>, <num_months>)
```

## Syntax Elements

**date** The date that is incremented. **num_months** The number of months by which to increment the date.

## Description

Computes the specified date plus the specified number of months. If the input date is the last day of the input month, then the output date is set to the last day of the output month.

To compute the date plus months without using the last day of the month functionality, use the ADD_MONTHS function.

The parameter `<date>` must be implicitly or explicitly converted to one of the following SQL data types:

- DATE
- TIMESTAMP
- SECONDDATE

The SQL data type of the output parameters is the same as the SQL data type of the input parameters. For example, ADD_MONTHS_LAST(DATE) returns a date, while ADD_MONTHS_LAST(TIMESTAMP) returns a timestamp.

## Example

The following example increments the date 2009-02-28 (the last day in February), by one month, and returns the value 2009-03-31, (the last day of March).

```sql
SELECT ADD_MONTHS_LAST (TO_DATE ('2009-02-28', 'YYYY-MM-DD'), 1) "add months
last" FROM DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
