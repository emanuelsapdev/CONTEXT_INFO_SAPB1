# 6.2.301 M_SYSTEM_REPLICATION_TAKEOVER_HISTORY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2069–2071

Provides access to a history of HSR takeover executions.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| TAKEOVER_START_TIME | TIMESTAMP | Displays the start time of the takeover command. This value matches tenant takeovers that are executed within the same system takeover process. |
| TAKEOVER_END_TIME | TIMESTAMP | Displays the end time of the takeover command. |
| EXECUTION_START_TIME | TIMESTAMP | Displays the execution start time for takeover of the transaction domain. |
| EXECUTION_END_TIME | TIMESTAMP | Displays the execution end time for takeover of the transaction domain. |
| SITE_ID | INTEGER | Displays the generated ID of the secondary site at takeover time. |
| SITE _NAME | VARCHAR(64) | Displays the logical name provided by the site administrator at takeover time. |
| MASTER_NAMESERVER_HOST | VARCHAR(64) | Displays the master nameserver host at takeover time. |
| VERSION | VARCHAR(32) | Displays the SAP HANA version for the site that is executing the takeover. |
| SOURCE_SITE_ID | INTEGER | Displays the generated ID of the source site at takeover time. |
| SOURCE_SITE _NAME | VARCHAR(64) | Displays the logical name for the source site provided by the site administrator at takeover time. |
| SOURCE_MASTER_NAMESERVER_HOST | VARCHAR(64) | Displays the source site master name server host at takeover time. |
| SOURCE_VERSION | VARCHAR(32) | Displays the source site SAP HANA version. |
| TAKEOVER_TYPE | VARCHAR(10) | Displays how the system went online:<br>• ONLINE: an online takeover<br>• OFFLINE: an offline takeover<br>• TIMETRAVEL: a timetravel take over |
| REPLICATION_MODE | VARCHAR(16) | Displays the replication mode at take over time. |
| OPERATION_MODE | VARCHAR(32) | Displays the operation mode at take over time. |
| REPLICATION_STATUS | VARCHAR(16) | Displays the replication status at take over time. |
| LOG_POSITION | BIGINT | Displays the master log position, that has been reached by takeover. |
| LOG_POSITION_TIME | TIMESTAMP | Displays the time reached by the take over. |
| SHIPPED_LOG_POSITION | BIGINT | Displays the highest master log position that has been shipped before executing takeover. |
| SHIPPED_LOG_POSITION_TIME | TIMESTAMP | Displays the time of the last shipped log buffer before executing takeover. |
| COMMENTS | NVARCHAR(5000) | Displays a comment for the remote subscription. |

## Related Information

M_SYSTEM_OVERVIEW System View [→](M_SYSTEM_OVERVIEW-System-View.md) M_SYSTEM_REPLICATION System View [→](M_SYSTEM_REPLICATION-System-View.md)
