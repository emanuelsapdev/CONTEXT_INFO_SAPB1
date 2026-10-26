# 4.9.1.238 YEARS_BETWEEN Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 399–400

Computes the number of years between two specified dates.

## Syntax

```sql
YEARS_BETWEEN(<date_1>, <date_2>)
```

## Description

Computes the number of years between `<date_1>` and `<date_2>`. Returns NULL if either of `<date_1>` or `<date_2>` is NULL.

## Examples

The following example returns the value `2` for the years between the two specified dates:

```sql
 SELECT YEARS_BETWEEN(TO_DATE('2001-01-01'), TO_DATE('2003-03-14'))
"years_between" FROM DUMMY;
```

The following example returns the value `-2` for the years between the two specified dates

```sql
 SELECT YEARS_BETWEEN(TO_DATE('2003-10-03'), TO_DATE('2001-01-14'))
"years_between" FROM DUMMY;
```

The following example returns the value `1` for the years between the two specified dates

```sql
 SELECT YEARS_BETWEEN(TO_DATE('2001-10-15'), TO_DATE('2003-01-14'))
"years_between" FROM DUMMY;
```

The following example returns the value `1` for the years between the two specified dates

```sql
 SELECT YEARS_BETWEEN(TO_DATE('2001-10-13'), TO_DATE('2003-01-14'))
"years_between" FROM DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
