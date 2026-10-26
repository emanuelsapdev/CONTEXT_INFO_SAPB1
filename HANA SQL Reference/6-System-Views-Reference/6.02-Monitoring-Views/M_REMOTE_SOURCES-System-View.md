# 6.2.219 M_REMOTE_SOURCES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1948–1949

Provides remote source information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USER_NAME | NVARCHAR(256) | Displays the user name. |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name. |
| LAST_REFRESH_TIME | TIMESTAMP | Displays the last successful completion timestamp of the refresh operation. |
| REFRESH_START_TIME | TIMESTAMP | Displays the timestamp of when the refresh operation was executed. |
| REFRESH_STATUS | VARCHAR(32) | Displays the refresh operation status: STARTED, COMPLETED,RUNNING (GET OBJECTS), RUNNING (GET OB JECT DETAILS),FAILED, CANCELLED, or CLEARED. |
| REFRESH_ERROR_MESSAGE | NVARCHAR(2000) | Displays the exception message that occurred during the refresh operation. |

## Related Information

REMOTE_SOURCES System View [→](../6.01-System-Views/REMOTE_SOURCES-System-View.md) M_REMOTE_SOURCE_LATENCY_HISTORY System View [→](M_REMOTE_SOURCE_LATENCY_HISTORY-System-View.md) M_REMOTE_SOURCE_LATENCY_STATUS System View [→](M_REMOTE_SOURCE_LATENCY_STATUS-System-View.md) M_REMOTE_SOURCE_STATISTICS System View [→](M_REMOTE_SOURCE_STATISTICS-System-View.md) REMOTE_SOURCE_OBJECTS System View [→](../6.01-System-Views/REMOTE_SOURCE_OBJECTS-System-View.md) REMOTE_SOURCE_OBJECT_COLUMNS System View [→](../6.01-System-Views/REMOTE_SOURCE_OBJECT_COLUMNS-System-View.md) REMOTE_SOURCE_OBJECT_COLUMN_CONSTRAINTS System View [→](../6.01-System-Views/REMOTE_SOURCE_OBJECT_COLUMN_CONSTRAINTS-System-View.md) REMOTE_SOURCE_OBJECT_COLUMN_DESCRIPTIONS System View [→](../6.01-System-Views/REMOTE_SOURCE_OBJECT_COLUMN_DESCRIPTIONS-System-View.md) REMOTE_SOURCE_OBJECT_DESCRIPTIONS System View [→](../6.01-System-Views/REMOTE_SOURCE_OBJECT_DESCRIPTIONS-System-View.md)
