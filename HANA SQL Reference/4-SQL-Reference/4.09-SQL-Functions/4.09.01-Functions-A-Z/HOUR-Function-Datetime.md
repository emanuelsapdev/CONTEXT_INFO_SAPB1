# 4.9.1.92 HOUR Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 202–203

Returns an integer representation of the hour portion of the specified time.

## Syntax

```sql
HOUR(<time>)
```

## Description

Returns an integer representation of the hour portion of the specified time.

## Example

The following example returns the hour `12`:

```sql
SELECT HOUR ('12:34:56') "hour" FROM DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
