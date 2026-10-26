# 4.9.1.132 NANO100_BETWEEN Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 261–262

Computes the time difference between two dates to the precision of 0.1 microseconds.

## Syntax

```sql
NANO100_BETWEEN(<date_1>, <date_2>)
```

## Description

Computes the time difference between date arguments `<date_1>` and `<date_2>`, to the precision of 0.1 microseconds.

## Example

The following example returns `864000000000` as the time difference between the two specified dates:

```sql
SELECT NANO100_BETWEEN ('2013-01-30', '2013-01-31') "nano100 between" FROM DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
