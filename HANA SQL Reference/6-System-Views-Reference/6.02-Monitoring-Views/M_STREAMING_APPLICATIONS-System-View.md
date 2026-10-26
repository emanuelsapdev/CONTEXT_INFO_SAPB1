# 6.2.284 M_STREAMING_APPLICATIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2042–2044

Provides streaming application monitoring information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema in which the application is deployed. |
| APPLICATION_NAME | NVARCHAR(256) | Displays the name of the streaming application. |
| APPLICATION_TYPE | VARCHAR(32) | Displays the application type: PROJECT, HA_PROJECT, or TOOLKIT_ADAPTER. |
| APPLICATION_INSTANCE | INTEGER | Displays the instance number of the streaming aplication. |
| APPLICATION_INSTANCE_COUNT | INTEGER | Displays the number of instances that are running or that are started. |
| SERVER_ALIAS | NVARCHAR(256) | Displays the name of the service on which the application is running. |
| REQUESTED_STATUS | VARCHAR(32) | Displays the status the application is requested to be in by the client: STOP PED/STARTED_RUNNING. |
| CURRENT_STATUS | VARCHAR(32) | Displays the status that the application is currently in:<br>• START<br>• STARTING<br>• STARTED<br>• STARTED_RUNNING<br>• STOPPING<br>• STOPPED<br>• STOPPED_FAILED<br>• STOPPED_FAILED_START |
| IS_FAILOVER_ENABLED | VARCHAR(5) | Indicates whether or not the project should be started on another node if the project or node fails: TRUE/FALSE. |
| FAILURE_COUNT | INTEGER | Displays the number of failures that have occurred in the failure interval. |
| FAILURE_INTERVAL | INTEGER | Displays the failure interval, in seconds, in which the application is shut down if the failure count reaches the max failures per interval. |
| MAX_FAILURES_PER_INTERVAL | INTEGER | Displays the number of failures that can occur in the specified failure interval before the application is shutdown. |

## Related Information

M_STREAMING_PROJECT_STREAMS System View [→](M_STREAMING_PROJECT_STREAMS-System-View.md) M_STREAMING_SCHEMAS System View [→](M_STREAMING_SCHEMAS-System-View.md)
