# 4.9.1.129 MONTH Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 259

Returns the number of the month from the specified date.

## Syntax

```sql
MONTH(<date>)
```

## Description

Returns the number of the month from date `<date>`.

## Example

The following example returns the value `5`, the month for the date specified:

```sql
SELECT MONTH ('2011-05-30') "month" FROM DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
