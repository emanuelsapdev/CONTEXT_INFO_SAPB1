# 6.2.6 M_ADMISSION_CONTROL_QUEUES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1645–1646

Provides detailed information regarding queued session requests by Session-Wise Admission Control.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| MESSAGE_ID | BIGINT | Displays the request ID of the client packet. |
| CONNECTION_ID | INTEGER | Displays the session connection ID. |
| MESSAGE_TYPE | VARCHAR(32) | Displays the request type. |
| STATEMENT_TYPE | VARCHAR(8) | Displays the statement type (for example, DDL or DML). |
| ENQUEUE_TIME | TIMESTAMP | Displays the request queue time in microseconds. |
| TIMEOUT_TIME | TIMESTAMP | Displays the estimated time, in microseconds, when the request should be timed-out. |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |

## Related Information

M_ADMISSION_CONTROL_EVENTS System View [→](M_ADMISSION_CONTROL_EVENTS-System-View.md) M_ADMISSION_CONTROL_STATISTICS System View [→](M_ADMISSION_CONTROL_STATISTICS-System-View.md)
