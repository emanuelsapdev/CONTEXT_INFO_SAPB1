# 6.2.217 M_RECOVERY_PROGRESS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1946–1947

Shows the progress of the most recent recoveries of tenant databases. M_RECOVERY_PROGRESS is in the SYS_DATABASES schema of a system database.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| DATABASE_NAME | VARCHAR(256) | Name of the tenant database. |
| BACKUP_ID | BIGINT | The unique ID of a recovery. |
| HOST | VARCHAR(64) | The host name. |
| PORT | SMALLINT | The internal port. |
| SERVICE_NAME | VARCHAR(32) | The name of the service. |
| SYS_START_TIME | TIMESTAMP | The time the recovery was started (local server time) |
| UTC_START_TIME | TIMESTAMP | The time the recovery was started (UTC) |
| SYS_END_TIME | TIMESTAMP | The time the recovery was completed (local server time) |
| UTC_END_TIME | TIMESTAMP | The time the recovery was completed (UTC) |
| STATE_NAME | VARCHAR(64) | The current state of the recovery |
| PHASE_NAME | VARCHAR(64) | The name of the current phase<br>A phase can be the databackup recovery, log backup recovery, restart, or and add or remove a service (if applicable). |
| MAX_PHASE | TINYINT | The number of phases to pass |
| CURRENT_PHASE | TINYINT | The number of the current phase |
| SYS_REACHED_TIME | TIMESTAMP | Point in time reached (local server time) |
| UTC_REACHED_TIME | TIMESTAMP | Point in time reached (UTC) |
| MESSAGE | VARCHAR(512) | Message that provides a possible reason as to why a recovery failed. |
| MAX_PROGRESS | BIGINT | Number of bytes still to be recovered. |
| CURRENT_PROGRESS | BIGINT | Number of bytes already recovered. |

## Related Information

[M_BACKUP_CATALOG System View](M_BACKUP_CATALOG-System-View.md)
