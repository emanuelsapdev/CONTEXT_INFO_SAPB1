# 6.2.187 M_MVCC_SNAPSHOTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1912–1913

Provides detailed snapshot information of the Multiversion Concurrency Control (MVCC) manager.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| TRANSACTION_ID | BIGINT | Displays the associated transaction object ID. |
| MVCC_SNAPSHOT_TIMESTAMP | BIGINT | Displays the MVCC timestamp of the snapshot. |
| STATEMENT_ID | BIGINT | Displays the associated logical statement ID. |
| RELATED_TABLES | VARCHAR(1024) | Displays the associated table object IDs. |

## Related Information

CURRENT_MVCC_SNAPSHOT_TIMESTAMP Function (Datetime) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_MVCC_SNAPSHOT_TIMESTAMP-Function-Datetime.md) M_MVCC_OVERVIEW System View [→](M_MVCC_OVERVIEW-System-View.md) M_MVCC_TABLES System View [→](M_MVCC_TABLES-System-View.md) M_SNAPSHOTS System View [→](M_SNAPSHOTS-System-View.md) M_TABLE_SNAPSHOTS System View [→](M_TABLE_SNAPSHOTS-System-View.md) M_TRANS_TOKENS System View [→](M_TRANS_TOKENS-System-View.md) BACKUP DATA CREATE SNAPSHOT Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/BACKUP-DATA-CREATE-SNAPSHOT-Statement-Backup-and-Recovery.md) BACKUP DATA DROP SNAPSHOT Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/BACKUP-DATA-DROP-SNAPSHOT-Statement-Backup-and-Recovery.md) BACKUP DATA CLOSE SNAPSHOT Statement (Backup and Recovery) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/BACKUP-DATA-CLOSE-SNAPSHOT-Statement-Backup-and-Recovery.md)
