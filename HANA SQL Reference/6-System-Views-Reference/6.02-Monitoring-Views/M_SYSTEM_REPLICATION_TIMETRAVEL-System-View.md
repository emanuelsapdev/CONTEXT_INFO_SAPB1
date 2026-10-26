# 6.2.302 M_SYSTEM_REPLICATION_TIMETRAVEL System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2071–2072

Provides information about the valid time travel range for each service on a secondary site.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| START_SNAPSHOT_ID | INTEGER | Displays the snapshot ID of the oldest commit timestamp on which timetravel can start. |
| START_TIME | TIMESTAMP | Displays the oldest commit timestamp on which timetravel can start. |
| START_REDO_LOG_POSITION | BIGINT | Displays the oldest log position on which timetravel can start. |
| END_TIME | TIMESTAMP | Displays the newest commit timestamp which can be reached via timetravel. |
| END_REDO_LOG_POSITION | BIGINT | Displays the newest log position that can be reached via timetravel. |
| COORDINATOR_TYPE | VARCHAR(16) | Displays the coordinator type: MASTER if it is a transaction master volume type or NONE if it is not a coordinator volume type. |

## Related Information

M_SYSTEM_OVERVIEW System View [→](M_SYSTEM_OVERVIEW-System-View.md) M_SYSTEM_REPLICATION System View [→](M_SYSTEM_REPLICATION-System-View.md)
