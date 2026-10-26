# 4.9.1.70 DAYS_BETWEEN Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 176–178

Computes the number of entire (24 hour) days between two dates.

## Syntax

```sql
DAYS_BETWEEN(<date_1>, <date_2>)
```

## Syntax Elements

#### date_1

Specifies the starting TIMESTAMP for the comparison.

#### date_2

Specifies the ending TIMESTAMP for the comparison.

## Description

Computes the number of entire days between `<date_1>` and `<date_2>`.

## Example

The following example returns the value `31` for days between the two dates specified:

```sql
SELECT DAYS_BETWEEN (TO_DATE ('2009-12-05', 'YYYY-MM-DD'), TO_DATE('2010-01-05',
'YYYY-MM-DD')) "days between" FROM DUMMY;
```

The following example returns the value `0` for days between the two specified dates:

```sql
SELECT DAYS_BETWEEN('2018-02-07 23:00:00',  '2018-02-08 01:00:00') AS sinceDays
FROM dummy;
```

The following example returns the value `1` for days between the two specified dates:

```sql
SELECT DAYS_BETWEEN('2018-02-07 23:00:00',  '2018-02-08 23:00:00') AS sinceDays
FROM dummy;
```

## Related Information

Datetime Data Types [→](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md) SAP Note 2573900 - Changed Behavior of the DAYS_BETWEEN function in HANA 2.0 SPS03
