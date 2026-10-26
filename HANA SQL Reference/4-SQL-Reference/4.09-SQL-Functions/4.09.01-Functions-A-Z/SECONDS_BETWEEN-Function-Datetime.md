# 4.9.1.167 SECONDS_BETWEEN Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 306

Computes the number of seconds between two specified dates.

## Syntax

```sql
SECONDS_BETWEEN(<date_1>, <date_2>)
```

## Description

Computes the number of seconds between date arguments `<date_1>` and `<date_2>`, which is semantically equal to (`<date_2>` - `<date_1>`).

## Example

The following example returns the value `2,678,400` as the number of seconds between the two specified dates:

```sql
SELECT SECONDS_BETWEEN ('2009-12-05', '2010-01-05') "seconds between" FROM DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
