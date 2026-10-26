# 4.9.1.11 ADD_SECONDS Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 93–94

Computes the specified time plus the specified seconds.

## Syntax

```sql
ADD_SECONDS(<time>, <num_seconds>)
```

## Syntax Elements

**time** The time that is incremented.

#### num_seconds

The number of seconds to increment the time by. Fractional values are supported for milliseconds and microseconds:

- 1/1000 – milliseconds
- 1/1000000 - microseconds

## Description

Computes the specified time plus the number of specified seconds.

## Example

The example increments the TIMESTAMP `2012-01-01 23:30:45` by `60*30` seconds, and returns the value `2012-01-02 00:00:45.0`:

```sql
SELECT ADD_SECONDS (TO_TIMESTAMP ('2012-01-01 23:30:45'), 60*30) "add seconds"
FROM DUMMY;
```

## Related Information

Datetime Data Types [→](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md) ADD_NANO100 Function (Datetime) [→](ADD_NANO100-Function-Datetime.md)
