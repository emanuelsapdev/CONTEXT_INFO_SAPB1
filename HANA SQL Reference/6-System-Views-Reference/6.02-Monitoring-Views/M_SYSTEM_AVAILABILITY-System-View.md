# 6.2.294 M_SYSTEM_AVAILABILITY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2058–2061

Monitors the availability of the system.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| EVENT_TIME | TIMESTAMP | Displays the time that this event was originally traced. |
| GUID | NVARCHAR (36) | Displays the event guide. |
| IS_ORIGIN | VARCHAR (5) | Displays the original entry. |
| TRACE_HOST | VARCHAR (64) | Displays the host the trace file was read from. |
| EVENT_NAME | VARCHAR (32) | Displays the event name:<br>• database_add<br>• database_remove<br>• failover_begin<br>• failover_end<br>• host_remove_prepare<br>• host_remove_reorg<br>• host_remove_abort<br>• host_remove<br>• ping<br>• recovery_begin<br>• recovery_end<br>• service_remove<br>• service_remove_abort<br>• service_remove_prepare<br>• service_remove_reorg<br>• service_started<br>• service_starting<br>• service_stopped<br>• service_stopping<br>• service_unknown |
| EVENT_DETAIL | VARCHAR (256) | Displays any additional information. |
| ERROR_MESSAGE | VARCHAR (256) | Displays the error message. |
| SYSTEM_ACTIVE | VARCHAR (16) | Displays the system active status: NO, YES, UNKNOWN, STARTING, or STOP PING. |
| SYSTEM_STATUS | VARCHAR (16) | Displays the system status:<br>• ERROR<br>• IGNORE<br>• INFO<br>• OK<br>• WARNING |
| HOST | VARCHAR (64) | Displays the host that traced the event. |
| HOST_ACTIVE | VARCHAR (16) | Displays the host active status. |
| HOST_STATUS | VARCHAR (16) | Displays the host status. |
| DATABASE_NAME | VARCHAR (256) | Displays the database name. |
| DATABASE_ACTIVE | VARCHAR (16) | Displays the database active status. |
| SERVICE_NAME | VARCHAR (32) | Displays the service name. |
| PORT | INTEGER | Displays the service port. |
| VOLUME_ID | INTEGER | Displays the volume ID. |
| SERVICE_ACTIVE | VARCHAR (16) | Displays the service active status. |
| HOST_CONFIG_ROLES | VARCHAR (64) | Displays the configured host roles. |
| HOST_ACTUAL_ROLES | VARCHAR (64) | Displays the actual host roles. |
| STORAGE_CONFIG_PARTITION | INTEGER | Displays the configured storage partition. |
| STORAGE_ACTUAL_PARTITION | INTEGER | Displays the actual storage partition. |
| TARGET_HOST | VARCHAR (64) | Displays the failover target host. |
| TARGET_HOST_CONFIG_ROLES | VARCHAR (64) | Displays the target host configuration roles. |
| TARGET_HOST_ACTUAL_ROLES | VARCHAR (64) | Displays the target host actual roles. |
| TARGET_STORAGE_CONFIG_PARTITION | INTEGER | Displays the target storage configuration partition. |
| TARGET_STORAGE_ACTUAL_PARTITION | INTEGER | Displays the target storage actual partition. |
| SITE_ID | INTEGER | Displays the system replication site ID. |

## Related Information

M_SYSTEM_DATA_STATISTICS System View [→](M_SYSTEM_DATA_STATISTICS-System-View.md) M_SYSTEM_INFORMATION_STATEMENTS System View [→](M_SYSTEM_INFORMATION_STATEMENTS-System-View.md) M_SYSTEM_OVERVIEW System View [→](M_SYSTEM_OVERVIEW-System-View.md)
