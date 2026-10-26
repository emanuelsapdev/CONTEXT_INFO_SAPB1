# 4.10.1.19.41 ALTER SYSTEM RECLAIM LOG Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 530–531

Reclaims the disk space of unused log segments when the SAP HANA database has accumulated many log segments.

## Syntax

```sql
ALTER SYSTEM RECLAIM LOG
```

## Description

Log segment accumulation can be caused in several ways. For example, when automatic log backup is not operational for a long period or a log savepoint is blocked for an extended time. When such issues occur, use the ALTER SYSTEM RECLAIM LOG command, but only after the root cause of the log accumulation has been fixed.

## Example

Reclaim the disk space of unused log segments.

```sql
ALTER SYSTEM RECLAIM LOG;
```

## Related Information

[M_LOG_SEGMENTS System View](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_LOG_SEGMENTS-System-View.md)
