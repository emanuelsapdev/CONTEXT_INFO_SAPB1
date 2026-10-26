# 6.2.337 M_TRACE_CONFIGURATION System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2114–2115

Provides information about trace configuration statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| VOLUME_ID | INTEGER | Displays the Persistence Volume ID. |
| STATISTICS_NAME | VARCHAR(128) | Displays the statistics object name. |
| TRACE_DIRECTORY | VARCHAR(512) | Displays the default trace level. |
| FORMATTER | VARCHAR(16) | Displays the trace formatter name. |
| FILE_NAME_PREFIX | VARCHAR(512) | Displays the trace file name prefix. |
| ALERT_FORMATTER | VARCHAR(16) | Displays the alert trace formatter name. |
| ALERT_FILE_NAME_PREFIX | VARCHAR(512) | Displays the alert trace file name prefix. |
| TRACE_FLUSH_INTERVAL | INTEGER | Displays the trace flush interval in seconds. |
| ALERT_TRACE_LEVEL | VARCHAR(16) | The trace level for alert traces. |
| DEFAULT_TRACE_LEVEL | VARCHAR(16) | Displays the default trace level. |
| TRACE_BUFFER_SIZE | INTEGER | Displays the trace buffer size in bytes. |
| MAX_TRACE_FILE_SIZE | BIGINT | Displays the max trace file size in bytes. |
| MAX_TRACE_FILE_ID | INTEGER | Displays the max trace file ID. |
| MAX_TRACE_FILES | INTEGER | Displays the max trace files to keep. |
| ALERT_TRACE_BUFFER_SIZE | INTEGER | Displays the alert trace buffer size in bytes. |
| MAX_ALERT_TRACE_FILE_SIZE | BIGINT | Displays the max alert trace file size in bytes. |
| TRACE_COMPRESSION_INTERVAL | INTEGER | Displays the interval, in seconds, to check for trace files that need to be compressed. |

## Additional Information

This view has a resettable counterpart; you can see the values since the last reset in the M_TRACE_CONFIGURATION_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_TRACE_CONFIGURATION_RESET;`.

## Related Information

M_TRACE_CONFIGURATION_RESET System View [→](M_TRACE_CONFIGURATION_RESET-System-View.md) ALTER SYSTEM CLEAR TRACES Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-TRACES-Statement-System-Management.md) ALTER SYSTEM REMOVE TRACES Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REMOVE-TRACES-Statement-System-Management.md) M_SERVICE_TRACES System View [→](M_SERVICE_TRACES-System-View.md)
