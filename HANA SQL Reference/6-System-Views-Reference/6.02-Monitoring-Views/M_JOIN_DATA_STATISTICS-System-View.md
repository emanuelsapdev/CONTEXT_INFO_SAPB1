# 6.2.141 M_JOIN_DATA_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1836–1839

Provides column store join engine join statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME1 | NVARCHAR(256) | Displays the schema name of the first table |
| TABLE_NAME1 | NVARCHAR(256) | Displays the name of the first table |
| COLUMN_NAME1 | NVARCHAR(256) | Displays the column name of the first table |
| SCHEMA_NAME2 | NVARCHAR(256) | Displays the schema name of the second table. Join data statistics are not collected |
| TABLE_NAME2 | NVARCHAR(256) | Displays the name of the second table. |
| COLUMN_NAME2 | NVARCHAR(256) | Displays the column name of the second table. |
| LAST_REFRESH_TIME | TIMESTAMP | Displays the time when the statistics was last refreshed. |
| RECORD_COUNT1 | BIGINT | Displays the estimated total row count of the first table. For temporary tables, this value is always 0. |
| COUNT1 | BIGINT | Displays the number of not Null values of the column of the first table. |
| DISTINCT_COUNT1 | BIGINT | Displays the number of unique not Null values of the column of the first table. |
| VALUE_COUNTS1 | NVARCHAR(1000) | Displays a comma-separated sorted list of unique column value counts. An in complete output of the list is truncated by an asterisk sign. If a uniform distribution of column values is assumed, then there is exactly one value count because values are uniformly distributed and every value counts the same. |
| VALUE_COUNTS_FREQUENCIES1 | NVARCHAR(1000) | Displays a comma-separated list of frequencies of the first table's column values with the same count. Any frequency refers to that value count with a corresponding position in the list of value counts. An incomplete output of the list is truncated by an asterisk sign. If a uniform distribution of column values is assumed, then there is exactly one value frequency because values are uniformly distributed. Generally, this single frequency matches the distinct count. |
| MATCHING_VALUES_COUNTS1 | NVARCHAR(1000) | Displays a comma-separated list of counts of the first table's column values which find a join partner. Any matching values count refers to that value count with corresponding position in the list of value counts. An incomplete output of the list is truncated by an asterisk sign. If a uniform distribution of column values is assumed, then the matching values count the one and only value count that is calculated from the unified distribution of the value counts. |
| MEMORY_SIZE | BIGINT | Displays the memory size, in bytes, used by the join data statistics object. |

## Additional Information

Join data statistics are not collected for temporary tables, so the SCHEMA_NAME, TABLE_NAME, and COLUMN_NAME values for a temporary table are NULL.

## Related Information

ALTER SYSTEM CLEAR COLUMN JOIN DATA STATISTICS (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-COLUMN-JOIN-DATA-STATISTICS-System.md) M_JOINENGINE_STATISTICS System View [→](M_JOINENGINE_STATISTICS-System-View.md) M_JOIN_TRANSLATION_TABLES System View [→](M_JOIN_TRANSLATION_TABLES-System-View.md) M_TABLE_PRUNING_STATISTICS System View [→](M_TABLE_PRUNING_STATISTICS-System-View.md)
