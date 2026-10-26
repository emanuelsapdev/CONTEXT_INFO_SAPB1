# 6.1.167 TABLE_REPLICAS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1596–1597

Provides information about replicated tables and their replicas.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| SOURCE_TABLE_NAME | NVARCHAR(256) | Displays the source table name. |
| SOURCE_TABLE_TYPE | VARCHAR(16) | Displays the source table type. |
| REPLICA_SCHEMA_NAME | NVARCHAR(256) | Displays the replica schema name. |
| REPLICA_TABLE_NAME | NVARCHAR(256) | Displays the replica name. |
| REPLICA_TABLE_TYPE | VARCHAR(16) | Displays the replica table type. |
| REPLICA_TYPE | VARCHAR(16) | Displays the replica type. |
| HAS_DIFFERENT_PARTITIONS | VARCHAR(5) | Displays whether the replica table has different partitions from the source table. |
| HAS_DIFFERENT_COLUMNS | VARCHAR(5) | Displays whether the replica table has different columns from the source table. |

## Related Information

ALTER SYSTEM {ENABLE | DISABLE} ALL [ASYNCHRONOUS | SYNCHRONOUS] TABLE REPLICAS Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ENABLE-DISABLE-ALL-ASYNCHRONOUS-SYNCHRONOUS.md) M_TABLE_REPLICAS System View [→](../6.02-Monitoring-Views/M_TABLE_REPLICAS-System-View.md) M_TABLE_REPLICAS_RESET System View [→](../6.02-Monitoring-Views/M_TABLE_REPLICAS_RESET-System-View.md)
