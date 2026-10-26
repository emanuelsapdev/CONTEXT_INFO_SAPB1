# 4.9.1.80 EXTRACT Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 188–189

Returns the requested portion of a specified date.

## Syntax

```sql
EXTRACT( {YEAR | MONTH | DAY | HOUR | MINUTE | SECOND} FROM <date> )
```

## Description

Returns the requested portion from the specified date.

## Example

The following example returns the value `2010` for the year extracted from the specified date:

```sql
SELECT EXTRACT (YEAR FROM TO_DATE ('2010-01-04', 'YYYY-MM-DD')) "extract" FROM
DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
