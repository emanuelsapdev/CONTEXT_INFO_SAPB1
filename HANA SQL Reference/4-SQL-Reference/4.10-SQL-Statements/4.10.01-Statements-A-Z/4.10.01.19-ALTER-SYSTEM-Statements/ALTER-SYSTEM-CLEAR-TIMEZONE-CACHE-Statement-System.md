# 4.10.1.19.26 ALTER SYSTEM CLEAR TIMEZONE CACHE Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 510–511

Clears cached timezone definitions.

## Syntax

```sql
ALTER SYSTEM CLEAR TIMEZONE CACHE DATASET <timezone_dataset_string_literal>
```

## Syntax Elements

#### timezone_dataset_string_literal

Specifies the data to be cleared.

```sql
<timezone_dataset_string_literal> ::= { sap | platform }
```

##### sap

Specifies to clear the currently-used SAP HANA dataset.

##### platform

Specifies to clear the dataset provided by the operating system.

## Description

For efficiency purposes, timezone definitions are cached in internal structures for timestamp conversions such as UTC to local date and time. Use ALTER SYSTEM CLEAR TIMEZONE CACHE DATASET to clear out the cached timezone definitions when they become stale, for example when a timezone definition changes.

After executing this statement, the timezone cache contents are recreated for the respective data sources at the next access.

## Permissions

The SERVICE ADMIN privilege is required to execute this statement.

## Example

Clears all cached timezone definitions in the currently used 'sap' dataset.

```sql
ALTER SYSTEM CLEAR TIMEZONE CACHE DATASET 'sap';
```

## Related Information

[TIMEZONES System View](../../../../6-System-Views-Reference/6.01-System-Views/TIMEZONES-System-View.md)
