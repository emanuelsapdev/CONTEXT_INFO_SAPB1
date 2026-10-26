# 6.2.315 M_TABLE_PRUNING_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2089–2090

Provides an interface to access statistics for historical data. This data helps detect unexpectedly heavy historical processing by an application, including disclosure of unqualified historical queries as well as assessing the effectiveness of pruning.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| STATEMENT_ID | VARCHAR(20) | Displays the statement ID. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| PRUNING_CALLER | VARCHAR(20) | Displays the operation that initiated the pruning: SEARCH, OLAP ENGINE, JOIN ENGINE, TABLE UPDATE, SQL PLAN GENERATION, or SQL PLAN EXECU TION. |
| PRUNING_TYPE | VARCHAR(20) | Displays the type of pruning that was initiated: COMPILE TIME, RUNTIME STATIC, RANGE RESTRICTION, or RUN TIME DYNAMIC. |
| PRUNING_FILTER | NCLOB | Displays the predicate used for pruning. |
| TOTAL_CS_PART_COUNT | INTEGER | Displays the total number of column store partitions before pruning. |
| TOTAL_ES_PART_COUNT | INTEGER | Displays the total number of extended storage partitions before pruning. |
| PRUNED_CS_PART_COUNT | INTEGER | Displays the number of column store partitions after pruning. |
| PRUNED_CS_PAGE_LOADABLE_PART_COUNT | INTEGER | Displays the number of column store partitions using paged attributes after pruning. |
| PRUNED_ES_PART_COUNT | INTEGER | Displays the number of extended storage partitions after pruning. |
