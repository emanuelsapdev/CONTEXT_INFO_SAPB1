# 6.2.268 M_SNAPSHOTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2009–2010

Provides information about existing snapshots.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| ID | BIGINT | Displays the snapshot ID. |
| TIMESTAMP | TIMESTAMP | Displays the creation time. |
| PURPOSE | VARCHAR(24) | Displays why the snapshot was executed. |
| FOR_BACKUP | VARCHAR(5) | Displays if the snapshot was created for backup: TRUE/FALSE. |
| ANCHOR | BIGINT | Displays the anchor. |
| REDO_LOG_POSITION | BIGINT | Displays the redo log position corresponding to the snapshot. |
| LAST_COMMIT_TIME | TIMESTAMP | Displays the timestamp of the last commit of the snapshot. |

## Related Information

[M_DATABASES System View](M_DATABASES-System-View.md)
