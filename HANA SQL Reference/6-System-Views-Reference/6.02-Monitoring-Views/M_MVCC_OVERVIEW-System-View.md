# 6.2.186 M_MVCC_OVERVIEW System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1910–1912

Provides an overview of the row-store Multiversion Concurrency Control (MVCC) manager.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VERSION_COUNT | BIGINT | Displays the number of all versions in the host. |
| DATA_VERSION_COUNT | BIGINT | Displays the number of data versions per service. |
| METADATA_VERSION_COUNT | BIGINT | Displays the number of metadata versions per service. |
| MIN_MVCC_SNAPSHOT_TIMESTAMP | BIGINT | Displays the minimum MVCC time stamp which at least one transaction holds. |
| GLOBAL_MVCC_TIMESTAMP | BIGINT | Displays the current global MVCC time stamp. |
| MIN_READ_TRANSACTION_ID | BIGINT | Indicates that all active transactions can see the changes of TRANSACTION IDs less than or equal to MIN_READ_TRANSACTION_ID. |
| MIN_WRITE_TRANSACTION_ID | BIGINT | Indicates that all write transactions with a TRANSACTION ID less than or equal to MIN_WRITE_TRANSACTION_ID are closed. |
| NEXT_WRITE_TRANSACTION_ID | BIGINT | Displays the maximum TRANSACTION ID which is assigned to the next write transaction. |
| ACQUIRED_LOCK_COUNT | BIGINT | Displays the number of acquired records locks. |
| MAX_VERSIONS_PER_PARTITION | BIGINT | Displays the max number of versions per partition. |
| AVG_HASH_LINK_FOR_DATA_VERSIONS | REAL | Deprecated; do not use. |
| AVG_HASH_LINK_FOR_METADATA_VERSIONS | REAL | Deprecated; do not use. |

## Related Information

M_MVCC_SNAPSHOTS System View [→](M_MVCC_SNAPSHOTS-System-View.md) M_MVCC_TABLES System View [→](M_MVCC_TABLES-System-View.md) M_SYSTEM_REPLICATION_MVCC_HISTORY System View [→](M_SYSTEM_REPLICATION_MVCC_HISTORY-System-View.md) CURRENT_MVCC_SNAPSHOT_TIMESTAMP Function (Datetime) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_MVCC_SNAPSHOT_TIMESTAMP-Function-Datetime.md) ALTER SYSTEM RECLAIM FLEXIBLE TABLES Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RECLAIM-FLEXIBLE-TABLES-Statement-System.md)
