# 4.9.1.114 LOCALTOUTC Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 238–240

A timestamp parameter holding the time to be converted between UTC and local time.

## Syntax

```sql
LOCALTOUTC (<time> [, <timezone> [, <timezone_dataset>]])
```

## Syntax Elements

#### time

Specifies the time to be converted between UTC and local time.

```sql
<time> ::= <timestamp>
```

#### timezone

Specifies the timezone defining the local time. For a list of available timezones, see the TIMEZONES system view. If the local timezone is not explicitly specified, then the local timezone of the SAP HANA system is used.

```sql
<timezone> ::= <string_literal>
```

#### timezone_dataset

Specifies the dataset in which to search for the given timezone.

```sql
<timezone_dataset> ::= { sap | platform }
```

- `sap` searches in the dataset in the timezone definition tables. This is the default value. To use this value, import a timezone dataset (see SAP Note 1791342). If you use this value without importing a dataset, the function uses hardcoded fallback values. These fallback values are deprecated and will be removed in a future support package stack.
- `platform` searches in the dataset provided by the operating system.

## Description

Converts the local time `<time>` from a timezone to the UTC(GMT) time.

The usage of local timestamps is discouraged; use UTC times instead. The use of local times or conversion between local time zones might require additional handling in the application code.

## Examples

The following example returns the value `2012-01-01 06:00:00.0` for the UTC date and time:

```sql
SELECT LOCALTOUTC (TO_TIMESTAMP('2012-01-01 01:00:00', 'YYYY-MM-DD HH24:MI:SS'),
'EST') "localtoutc" FROM DUMMY;
```

The following example returns the value `2012-01-01 06:00:00.0` for the UTC date and time:

```sql
SELECT LOCALTOUTC (TO_TIMESTAMP('2012-01-01 01:00:00', 'YYYY-MM-DD HH24:MI:SS'),
'EST', 'sap') "localtoutc" FROM DUMMY;
```

## Related Information

TIMEZONES System View [→](../../../6-System-Views-Reference/6.01-System-Views/TIMEZONES-System-View.md) SAP Note 1791342
