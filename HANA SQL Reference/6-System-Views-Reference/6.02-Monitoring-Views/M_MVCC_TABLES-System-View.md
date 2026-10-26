# 6.2.188 M_MVCC_TABLES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1913

Provides statistics for the row-store Multiversion Concurrency Control (MVCC) manager.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| NAME | VARCHAR(256) | Displays the table name. |
| VALUE | VARCHAR(128) | Displays the value. |

## Related Information

M_MVCC_OVERVIEW System View [→](M_MVCC_OVERVIEW-System-View.md) M_MVCC_SNAPSHOTS System View [→](M_MVCC_SNAPSHOTS-System-View.md) M_TRANS_TOKENS System View [→](M_TRANS_TOKENS-System-View.md)
