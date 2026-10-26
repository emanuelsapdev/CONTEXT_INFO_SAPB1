# 6.2.5 M_ADMISSION_CONTROL_EVENTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1644–1645

Displays information about significant events.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| EVENT_TIME | TIMESTAMP | Displays the time of the event. |
| EVENT_TYPE | VARCHAR(32) | Displays the type of event. |
| EVENT_REASON | VARCHAR(64) | Displays the reason for the event. |
| QUEUE_WAIT_TIME | BIGINT | Displays the queue wait time, in microseconds. |
| CONNECTION_ID | INTEGER | Displays the session connection ID. |
| MESSAGE_TYPE | VARCHAR(32) | Displays the request type. |
| STATEMENT_ID | VARCHAR(20) | Displays the prepared statement ID. |
| STATEMENT_HASH | VARCHAR(32) | Displays the unique identifier for an SQL string. |
| CPU_USAGE_RATIO | INTEGER | Displays the measured value of the CPU usage. |
| MEMORY_RATIO | INTEGER | Displays the measured memory size, in bytes, as a percentage of the global allocation limit. |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |

## Related Information

M_ADMISSION_CONTROL_QUEUES System View [→](M_ADMISSION_CONTROL_QUEUES-System-View.md) M_ADMISSION_CONTROL_STATISTICS System View [→](M_ADMISSION_CONTROL_STATISTICS-System-View.md)
