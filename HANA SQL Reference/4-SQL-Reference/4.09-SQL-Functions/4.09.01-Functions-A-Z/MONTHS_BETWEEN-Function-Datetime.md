# 4.9.1.131 MONTHS_BETWEEN Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 260–261

Computes the number of months between two dates.

## Syntax

```sql
MONTHS_BETWEEN(<date_1>, <date_2>)
```

## Description

Computes the number of months between `<date_1>` and `<date_2>`. Returns NULL if either of `<date_1>` or `<date_2>` is NULL.

## Examples

The following example returns `2` for the months between the two dates:

```sql
SELECT MONTHS_BETWEEN(TO_DATE ('2003-01-01'), TO_DATE('2003-03-14'))
"months_between" FROM DUMMY;
```

The following example returns `-8` for the months between the two dates:

```sql
SELECT MONTHS_BETWEEN(TO_DATE ('2003-10-03'), TO_DATE('2003-01-14'))
"months_between" FROM DUMMY;
```

The following example returns `-9` for the months between the two dates:

```sql
SELECT MONTHS_BETWEEN(TO_DATE ('2003-10-15'), TO_DATE('2003-01-14'))
"months_between" FROM DUMMY;
```

The following example returns `-8` for the months between the two dates:

```sql
SELECT MONTHS_BETWEEN(TO_DATE ('2003-10-13'), TO_DATE('2003-01-14'))
"months_between" FROM DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
