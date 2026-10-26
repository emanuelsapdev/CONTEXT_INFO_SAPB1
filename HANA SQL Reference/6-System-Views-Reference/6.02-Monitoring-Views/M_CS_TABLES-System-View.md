# 6.2.68 M_CS_TABLES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1729–1734

Provides runtime data for column tables.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| PART_ID | INTEGER | Returns the table partition ID:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• For replicated tables, the part ID is 1 for the original table and subsequent part IDs are assigned to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is currently in progress. |
| MEMORY_SIZE_IN_TOTAL | BIGINT | Displays that the total memory size, in bytes, is the sum of memory size in the main, delta, and history parts. |
| MEMORY_SIZE_IN_MAIN | BIGINT | Displays the current memory consumption, in bytes, in main. This value varies depending on the number of attributes actually loaded and includes data for open transactions. |
| MEMORY_SIZE_IN_DELTA | BIGINT | Displays the current memory consumption, in bytes, in delta. |
| MEMORY_SIZE_IN_HISTORY_MAIN | BIGINT | Displays the current memory consumption, in bytes, in history-main. This value is 0 for normal, non-history tables. |
| MEMORY_SIZE_IN_HISTORY_DELTA | BIGINT | Displays the current memory consumption, in bytes, in history-delta. This value is 0 for normal non-history tables. |
| MEMORY_SIZE_IN_PAGE_LOADABLE_MAIN | BIGINT | Displays the total paged memory size of the table. |
| MEMORY_SIZE_IN_MISC | BIGINT | Displays the used memory size, in bytes, for the internal structures that are common to all columns in a table and that are not included in the MEMORY_SIZE_IN_MAIN or MEMORY_SIZE_IN_DELTA columns. |
| PERSISTENT_MEMORY_SIZE_IN_TOTAL | BIGINT | For columns stored in persistent memory, displays the total memory size in bytes. |
| ESTIMATED_MAX_MEMORY_SIZE_IN_TOTAL | BIGINT | Displays the estimated maximum memory consumption, in bytes, in total, for the fully loaded table (data for open transactions is not included). |
| LAST_ESTIMATED_MEMORY_SIZE | BIGINT | Displays the last estimated memory consumption, in bytes, for the fully loaded table. |
| LAST_ESTIMATED_MEMORY_SIZE_TIME | TIMESTAMP | Displays the last time the last estimated memory consumption was calculated. |
| RECORD_COUNT | BIGINT | Displays the record count. |
| RAW_RECORD_COUNT_IN_MAIN | BIGINT | Displays the current number of entries in the main part of the table. This value differs from the number of visible table main rows because there are entries for modified rows that are marked as invalidated. |
| RAW_RECORD_COUNT_IN_DELTA | BIGINT | Displays the current number of entries in the table delta part. This value differs from the number of visible table delta rows because there are additional en tries, such as deleted rows or updated rows. This column can contain deleted records. |
| RAW_RECORD_COUNT_IN_HISTORY_MAIN | BIGINT | Displays the raw record count in history-main. |
| RAW_RECORD_COUNT_IN_HISTORY_DELTA | BIGINT | Displays the raw record count in history-delta. |
| LAST_COMPRESSED_RECORD_COUNT | BIGINT | Displays the number of entries in main during the last optimize compression run. |
| MAX_UDIV | BIGINT | Displays the maximum table row number. This number is for internal use only. |
| MAX_MERGE_CID | BIGINT | Displays the maximum commit-ID of transactions for which changes were already merged into the main table. |
| MAX_ROWID | BIGINT | Displays the maximum row ID. This number is purely technical and only used internally. |
| IS_DELTA2_ACTIVE | VARCHAR(5) | Indicates whether a second delta is used: TRUE/FALSE. During a table delta merge, updates and inserts are stored to a second delta because the first delta is locked. |
| IS_DELTA_LOADED | VARCHAR(5) | Indicates whether the delta part of the table is loaded: TRUE/FALSE. |
| IS_LOG_DELTA | VARCHAR(5) | Indicates whether that currently the redo log is currently being written: TRUE/FALSE. |
| PERSISTENT_MERGE | VARCHAR(5) | Indicates whether the new main part will be written to the disk during a table delta merge, unless requested differ ently: TRUE/FALSE. |
| CREATE_TIME | TIMESTAMP | Displays the creation time. |
| MODIFY_TIME | TIMESTAMP | Displays the latest modify timestamp of any column store table run time data. This value is used to trigger invalidation of related translation tables used by the column store join operations. |
| LAST_MERGE_TIME | TIMESTAMP | Displays the point in time, in UNIX time format, of the last time the table delta part was merged into the main part. |
| LAST_REPLAY_LOG_TIME | TIMESTAMP | Displays the point in time, in UNIX time format, of the last time the table log was replayed. |
| LAST_TRUNCATION_TIME | TIMESTAMP | Displays the last time the table was truncated. |
| LAST_CONSISTENCY_CHECK_TIME | TIMESTAMP | Displays the last time the table consistency was checked with the CHECK_TABLE_CONSISTENCY procedure. |
| LAST_CONSISTENCY_CHECK_ERROR_COUNT | BIGINT | Displays the number of errors found in the last table consistency check. |
| LOADED | VARCHAR(10) | Displays the flag to show how many columns of the table are loaded in memory: NO, PARTIALLY, and FULL. See M_CS_COLUMNS for each column. |
| LOAD_UNIT | VARCHAR(7) | Displays the load unit for the table: PAGE, COLUMN, and UNKNOWN. |
| READ_COUNT | BIGINT | Displays the number of read accesses on the table or partition.<br>This is not the number of SELECT statements against this table. A SELECT statement may involve several read accesses. |
| WRITE_COUNT | BIGINT | Displays the number of write accesses on the table or partition.<br>This is not the number of DML and DDL statements against this table. A DML or DDL statement may involve several write accesses. |
| MERGE_COUNT | BIGINT | Displays the number of delta merges done on the table or partition. |
| IS_REPLICA | VARCHAR(5) | Displays the flag to indicate that the part is a replica. |
| UNUSED_RETENTION_PERIOD | INTEGER | Displays the unused retention period. |
| HAS_RECORD_COMMIT_TIMESTAMP | VARCHAR(5) | Displays whether the table is tracking commit timestamps: TRUE or FALSE. |
| PERSISTENT_MEMORY | VARCHAR(5) | Displays the persistent memory preference inferred from userspecified preferences in bottom-up manner starting from this object: TRUE/FALSE. |

## Additional Information

While the counter MERGE_COUNT counts merges of the table since the instance started, the corresponding LAST_MERGE_TIME timestamp persists permanently. Consequently, it is possible to see entries that have MERGE_COUNT = 0 and LAST_MERGE_TIME at some TIMESTAMP in the past. Additionally, when you copy a column store table (via CREATE COLUMN TABLE… LIKE … ) the LAST_MERGE_TIME of the original table gets copied, and the MERGE_COUNT of the new table is set to 0.

## Related Information

M_CS_COLUMNS System View [→](M_CS_COLUMNS-System-View.md) TABLES System View [→](../6.01-System-Views/TABLES-System-View.md) CREATE TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/README.md) LOCK TABLE Statement (Transaction Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/LOCK-TABLE-Statement-Transaction-Management.md) RENAME TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RENAME-TABLE-Statement-Data-Definition.md) ALTER TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.20-ALTER-TABLE/README.md) TRUNCATE TABLE Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/TRUNCATE-TABLE-Statement-Data-Manipulation.md) DROP TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-TABLE-Statement-Data-Definition.md)
