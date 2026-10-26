# 6.2.300 M_SYSTEM_REPLICATION_MVCC_HISTORY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2068–2069

Displays the global multi-version concurrency control (MVCC) timestamp history in the secondary site for system replication. The global MVCC timestamp of the secondary site is updated after a chunk of logs from the primary site is replayed on the secondary site.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| GLOBAL_MVCC_TIMESTAMP | BIGINT | Displays the global MVCC timestamp |
| SECONDARY_SITE_TIME | TIMESTAMP | Displays the global MVCC timestamp updated time of the secondary site |
| PRIMARY_SITE_TIME | TIMESTAMP | Displays the global MVCC updated time of the primary site |
| SECONDARY_SITE_UPDATE_DURATION | BIGINT | Displays the global MVCC update duration of the secondary site in milliseconds |

## Related Information

M_SYSTEM_REPLICATION System View [→](M_SYSTEM_REPLICATION-System-View.md) M_MVCC_OVERVIEW System View [→](M_MVCC_OVERVIEW-System-View.md) M_MVCC_SNAPSHOTS System View [→](M_MVCC_SNAPSHOTS-System-View.md) M_MVCC_TABLES System View [→](M_MVCC_TABLES-System-View.md) ALTER SYSTEM {ENABLE | DISABLE} SYSTEM REPLICATION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ENABLE-DISABLE-SYSTEM-REPLICATION-Statement.md)
