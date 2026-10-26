# 6.1.170 TEMPORAL_TABLES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1600–1601

Provides information about system-versioned tables, history tables, and application-time period tables.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| PERIOD_NAME | NVARCHAR(256) | Displays the period name. |
| PERIOD_START_COLUMN | NVARCHAR(256) | Displays the period start column name. |
| PERIOD_END_COLUMN | NVARCHAR(256) | Displays the period end column name. |
| HAS_TIMELINE_INDEX | VARCHAR(5) | For internal use only. |
| HISTORY_SCHEMA_NAME | VARCHAR(256) | Displays the schema of the history table associated to the system-versioned table. |
| HISTORY_TABLE_NAME | NVARCHAR(256) | Displays the name of the history table associated to the system-versioned table. |

## Related Information

[TABLES System View](TABLES-System-View.md)
