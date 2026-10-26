# 4.9.1.69 DAYOFYEAR Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 176

Returns an integer representation of the day of the year for the specified date.

## Syntax

```sql
DAYOFYEAR(<date>)
```

## Description

Returns an integer representation of the day of the year for the specified date.

## Example

The following example returns the value `150` as the day of the year for the specified date:

```sql
SELECT DAYOFYEAR ('2011-05-30') "dayofyear" FROM DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
