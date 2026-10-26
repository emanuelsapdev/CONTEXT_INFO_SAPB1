# 4.10.1.19.52 ALTER SYSTEM SAVEPOINT Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 542–543

Executes a database checkpoint on the persistence manager.

## Syntax

```sql
ALTER SYSTEM SAVEPOINT
```

## Description

A savepoint is a point in time when a complete consistent image of the database is persisted to the disk. The consistent image can be used to restart the database.

Normally a savepoint is executed periodically as configured by the configuration parameter `savepoint_interval_s` in the [persistence] section. For special (normal test) purposes, the savepoint can be disabled. In this case, use this command to manually execute a savepoint.

The views associated with the ALTER SYSTEM SAVEPOINT statement are: M_SAVEPOINTS, M_SAVEPOINT_STATISTICS, M_SAVEPOINT_STATISTICS_RESET, and HOST_SAVEPOINTS.

This statement should not be confused with the SAVEPOINT statement, which performs a transactional savepoint.

## Example

Execute a savepoint on the persistence manager.

```sql
ALTER SYSTEM SAVEPOINT;
```

## Related Information

M_SAVEPOINT_STATISTICS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SAVEPOINT_STATISTICS-System-View.md) M_SAVEPOINT_STATISTICS_RESET System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SAVEPOINT_STATISTICS_RESET-System-View.md) M_SAVEPOINTS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SAVEPOINTS-System-View.md) SAVEPOINT Statement (Transaction Management) [→](../SAVEPOINT-Statement-Transaction-Management.md)
