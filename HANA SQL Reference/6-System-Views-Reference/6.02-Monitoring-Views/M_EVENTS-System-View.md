# 6.2.108 M_EVENTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1788–1790

Provides information about internal events.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host. |
| PORT | INTEGER | Displays the port. |
| SOURCE_HOST | VARCHAR(64) | Displays the original host if the event was created via another host. |
| SOURCE_PORT | INTEGER | Displays the original port if the event was created via another host. |
| TYPE | VARCHAR(256) | Displays the type of event. |
| ID | BIGINT | Displays the ID of the event. |
| INFOTEXT | VARCHAR(2000) | Displays additional information in free text. |
| CREATE_TIME | TIMESTAMP | Displays the time that the event was created. |
| UPDATE_TIME | TIMESTAMP | Displays the time that the event was updated. |
| HANDLE_TIME | TIMESTAMP | Displays the time that the event was handled. |
| STATE | VARCHAR(256) | Displays the state of the event. |
| ACKNOWLEDGED | VARCHAR(5) | Indicates whether the event is acknowl edged: TRUE/FALSE. |
| FAILED_HANDLES | BIGINT | Displays the number of failed handle attempts. |

## Additional Information

Important events (for example, DiskFull) reported by the database are shown in this view. The state of an event can be either NEW or HANDLED. CREATE TIME shows the time the event was created (and reported) and HANDLE time shows the time the event was handled (that is, cleared). Handled events are removed periodically by the StatisticsServer

## Related Information

[ALL_AUDIT_LOG System View](../6.01-System-Views/ALL_AUDIT_LOG-System-View.md)
