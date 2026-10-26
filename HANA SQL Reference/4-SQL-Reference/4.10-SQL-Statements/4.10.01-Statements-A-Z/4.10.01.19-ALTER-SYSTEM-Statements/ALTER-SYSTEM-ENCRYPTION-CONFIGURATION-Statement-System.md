# 4.10.1.19.31 ALTER SYSTEM ENCRYPTION CONFIGURATION Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 517–518

Controls encryption configuration for tenant databases.

## Syntax

```sql
ALTER SYSTEM ENCRYPTION CONFIGURATION CONTROLLED BY { SYSTEM DATABASE | LOCAL
DATABASES }
```

## Syntax Elements

#### SYSTEM DATABASE

Run on the tenant database, specifies that encryption configuration is controlled by the system database. Use this syntax on the tenant database to change control over to the system database.

#### LOCAL DATABASES

Specifies that encryption configuration is controlled by the tenant databases. Use this syntax on the system database to change control over to the tenant databases.

## Description

Controls encryption configuration for tenant databases.

To determine which database is controlling encryption configuration for a tenant database, check the relevant value in the CONFIGURATION_CONTROL column of the M_ENCRYPTION_OVERVIEW system view.

## Examples

When run on the system database, this statement gives control of encryption configuration to the tenant databases:

```sql
ALTER SYSTEM ENCRYPTION CONFIGURATION CONTROLLED BY LOCAL DATABASES;
```

When run on a tenant database, the following statement gives control of encryption configuration to the system databases:

```sql
ALTER SYSTEM ENCRYPTION CONFIGURATION CONTROLLED BY SYSTEM DATABASE;
```

## Related Information

[M_ENCRYPTION_OVERVIEW System View](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_ENCRYPTION_OVERVIEW-System-View.md)
