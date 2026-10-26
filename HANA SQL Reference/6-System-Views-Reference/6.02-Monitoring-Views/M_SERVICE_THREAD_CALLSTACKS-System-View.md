# 6.2.262 M_SERVICE_THREAD_CALLSTACKS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2002–2003

Provides stack frame information for service threads.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SERVICE_NAME | VARCHAR(32) | Displays the service name. See M_SERVICE_TYPES for all known service names. |
| THREAD_ID | BIGINT | Displays the thread ID. |
| IS_ACTIVE | VARCHAR(5) | Displays whether the thread is active. |
| FRAME_LEVEL | INTEGER | Displays the level of the stack frame. |
| FRAME_NAME | VARCHAR(256) | Displays the name of stack frame (function, file, library, and so on). |

## Additional Information

While this view is publicly visible, its contents can only be seen by users with the DATABASE ADMIN privilege.

## Related Information

M_SERVICE_TYPES System View [→](M_SERVICE_TYPES-System-View.md) M_SERVICE_THREADS System View [→](M_SERVICE_THREADS-System-View.md) M_SERVICE_THREAD_SAMPLES System View [→](M_SERVICE_THREAD_SAMPLES-System-View.md)
