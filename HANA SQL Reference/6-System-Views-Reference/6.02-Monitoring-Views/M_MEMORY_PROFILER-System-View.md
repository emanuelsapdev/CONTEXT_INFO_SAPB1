# 6.2.176 M_MEMORY_PROFILER System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1896–1897

Provides memory profiler information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| FILE_NAME | VARCHAR(256) | Displays the file name. |
| PROFILE_NAME | VARCHAR(64) | Displays the profile name. |
| SERVICE_NAME | VARCHAR(32) | Displays the service name. |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| SAMPLING_INTERVAL | INTEGER | Displays the sampling interval in milliseconds. |
| START_TIME | TIMESTAMP | Displays the start time. |
| STOPE_TIME | TIMESTAMP | Displays the stop time. |
| REMAINING_SECONDS | INTEGER | Displays the remaining seconds until an automatic stop. |
| STATUS | VARCHAR(16) | Displays the status: STARTED/STOP PED. |
| HAS_CALLSTACKS | VARCHAR(5) | Indicates whether or not the profiler has callstacks recorded: TRUE/FALSE. |
| FILE_SIZE | BIGINT | Displays the size of the file in bytes. |

## Related Information

M_MEMORY System View [→](M_MEMORY-System-View.md) ALTER SYSTEM {START | STOP | SAVE | CLEAR} KERNEL PROFILER Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-START-STOP-SAVE-CLEAR-KERNEL-PROFILER.md)
