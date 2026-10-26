# 4.9.1.166 SECOND Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 305–306

Returns the second portion of a specified time.

## Syntax

```sql
SECOND(<time>)
```

## Description

Returns a value of seconds for a given time.

Subseconds are included for TIMESTAMP datatypes.

## Examples

The following example returns the value `56` for the seconds of the specified time:

```sql
SELECT SECOND ('12:34:56') "second" FROM DUMMY;
```

The following example returns the value `56.789` for the subseconds of the specified time:

```sql
SELECT SECOND ('2014-03-25 12:34:56.789') "subseconds" FROM DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
