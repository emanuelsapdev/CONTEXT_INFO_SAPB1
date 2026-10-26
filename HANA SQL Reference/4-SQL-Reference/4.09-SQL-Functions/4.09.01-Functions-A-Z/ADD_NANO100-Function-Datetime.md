# 4.9.1.10 ADD_NANO100 Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 92–93

Adds the specified number of 10^-7 unit of seconds to the specified TIMESTAMP value.

## Syntax

```sql
ADD_NANO100( <time>, <num> )
```

## Syntax Elements

**time** The TIMESTAMP value to add the units of seconds to. **num** The number of 10^-7 unit of seconds to increment the TIMESTAMP value by.

## Description

Computes the specified TIMESTAMP value plus the specified number of microseconds.

## Example

The following example increments the TIMESTAMP value by `864000000000` microseconds and returns `1000-01-02 10:00:00.0000000`:

```sql
SELECT ADD_NANO100(TO_TIMESTAMP('1000-01-01 10:00:00.0000000'), 864000000000)
FROM DUMMY;
```

The following example increments the TIMESTAMP value by `1` microsecond and returns `1000-01-01 10:00:00.0000001`:

```sql
SELECT ADD_NANO100(TO_TIMESTAMP('1000-01-01 10:00:00.0000000'), 1) FROM DUMMY;
```

## Related Information

[ADD_SECONDS Function (Datetime)](ADD_SECONDS-Function-Datetime.md)
