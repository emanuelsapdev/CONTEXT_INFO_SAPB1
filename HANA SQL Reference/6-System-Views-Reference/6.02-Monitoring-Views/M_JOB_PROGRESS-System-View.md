# 6.2.139 M_JOB_PROGRESS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1833–1835

Provides information about current long running system operations.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema of the object. |
| OBJECT_NAME | NVARCHAR(256) | Displays the name of the object. |
| JOB_NAME | NVARCHAR(128) | Displays the type of operation. See the table below for more detail. |
| CONNECTION_ID | INTEGER | Displays the connection that triggered the operation. |
| START_TIME | TIMESTAMP | Displays the start time of the operation. |
| CURRENT_PROGRESS | INTEGER | Displays the steps of the operation that are already finished. |
| MAX_PROGRESS | INTEGER | Displays the maximum operation progress. |
| PROGRESS_DETAIL | NVARCHAR(256) | Displays the detailed information about the operation. |

## Additional Information

The below table lists the possible types of job operations:

| **Column name** | **Description** |
| --- | --- |

JOB_NAME ● Alter Column Load Unit: Convert/change load unit at

the column level using NSE DDLs.

- Alter Index Load Unit: Convert/change load unit at the index level using NSE DDLs.
- Alter Partition Load Unit: Convert/change load unit at the partition level using NSE DDLs.
- Alter Table Load Unit: Convert/change load unit at the table level using NSE DDLs.
- BW F Fact Table Compression: fact table compression
- Backup: data backup
- Check Table Consistency: table consistency check
- Column table reloading on startup: Column table re loading on startup
- Create Index: index creation
- DSO activation: dso activation
- DSO conversion: dso conversion
- DSO rollback: dso rollback
- Data Statistics Autocreate: Automatic creation of data statistics
- Delta Log Replay: delta log replay
- Delta Merge: delta merge
- Export All: main export operation
- Export Object: exporting data for an object invoked by 'Export All'
- Import All: main import operation
- Import Object: importing data for an object invoked by 'Import All'
- Memory Profiler: load memory profiler data into tables
- Move Table: table move
- Online Repartitioning: allows DML workloads during DDL executions
- Optimize Compression: optimize compression
- Plan Stability: Execute all cached plans to capture
- Re-partitioning: table split and merge operations
- Reclaim Delta: reclaim rows from delta which are not visible
- Row Store Reorganization: row storage reorganization
- Runtimedump: Runtimedump
- Save PerfTrace: saving performance trace

| **Column name** | **Description** |
| --- | --- |
|   | • Savepoint Critical Phase: critical phase of savepoint<br>• Savepoint: savepoint<br>• System Replication Data Transfer: system replication full data and delta data/log shipping<br>• Table Consistency Check: Table Consistency Checks (Procedure CHECK_TABLE_CONSISTENCY)<br>• Table Redistribution Execute: table redistribution plan execution<br>• Table Redistribution Generate: table redistribution plan generation<br>• Table conversion (Col to Row): table type conversion from column to row store<br>• Table conversion (Row to Col): table type conversion from row to column store |

## Related Information

[M_JOB_HISTORY_INFO System View](M_JOB_HISTORY_INFO-System-View.md)
