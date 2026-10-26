# 6.2.285 M_STREAMING_PROJECTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2044–2046

Provides streaming project monitoring information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema in which the application is deployed. |
| PROJECT_NAME | NVARCHAR(256) | Displays the name given to the project. |
| PROJECT_INSTANCE | INTEGER | Displays the instance number of the project. |
| CPU_UTILIZATION | REAL | Displays the total CPU usage, as a percentage, by the project since the last update. These values range from 0 to 100. |
| CPU_SYSTEM_UTILIZATION | REAL | Displays the total system CPU usage, as a percentage, by the project since the last update. These values range from 0 to 100. |
| CPU_USER_UTILIZATION | REAL | Displays the total user CPU usage, as a percentage, by the project since the last update. These values range from 0 to 100. |
| TOTAL_CPU_TIME | BIGINT | Displays the total CPU time, in microseconds, used by the project since it started. |
| TOTAL_CPU_SYSTEM_TIME | BIGINT | Displays the total system CPU time, in microseconds, used by the project since it started. |
| TOTAL_CPU_USER_TIME | BIGINT | Displays the total user CPU time, in microseconds, used by the project since it started. |
| PROJECT_DURATION | BIGINT | Displays the number of microseconds since the project started. |
| VIRTUAL_MEMORY_SIZE | BIGINT | Displays the total amount of virtual memory used by the project in bytes. |
| RESIDENT_MEMORY_SIZE | BIGINT | Displays the total amount of resident memory used by the project in bytes. |
| THREAD_COUNT | INTEGER | Displays the total number of threads used by the project at the time of the update. |
| MONITORING_INTERVAL | INTEGER | Displays how often stream/client statistics are gathered in seconds. |
| IS_ACTIVE_ACTIVE_ENABLED | VARCHAR(5) | Indicates if the Active/Active (Read Enabled) high availibility mode is enabled for the project: TRUE/FALSE. |
| ACTIVE_ACTIVE_ROLE | VARCHAR(16) | Indicates whether the project instance plays the primary or secondary role in the Active/Active (Read Enabled) high availibility mode. |
| LAST_UPDATE_TIME | TIMESTAMP | Displays the last time that the statistics were updated for the project. |

## Related Information

M_STREAMING_PROJECT_ADAPTERS System View [→](M_STREAMING_PROJECT_ADAPTERS-System-View.md) M_STREAMING_PROJECT_ADAPTER_STATISTICS System View [→](M_STREAMING_PROJECT_ADAPTER_STATISTICS-System-View.md) M_STREAMING_PROJECT_GD_SUBSCRIPTIONS System View [→](M_STREAMING_PROJECT_GD_SUBSCRIPTIONS-System-View.md) M_STREAMING_PROJECT_PUBLISHERS System View [→](M_STREAMING_PROJECT_PUBLISHERS-System-View.md) M_STREAMING_PROJECT_STREAMS System View [→](M_STREAMING_PROJECT_STREAMS-System-View.md) M_STREAMING_PROJECT_SUBSCRIBERS System View [→](M_STREAMING_PROJECT_SUBSCRIBERS-System-View.md)
