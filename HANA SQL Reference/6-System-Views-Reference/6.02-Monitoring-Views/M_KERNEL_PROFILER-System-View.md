# 6.2.143 M_KERNEL_PROFILER System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1841–1842

Displays the state and provides information about Kernel Profilers in the system. You must have the RESOURCE ADMIN or TRACE ADMIN system privileges to use this view.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| APPLICATION_USER_NAME | NVARCHAR(256) | Displays the application user name to filter on. |
| USER_NAME | NVARCHAR(256) | Displays the SQL user name to filter on. |
| WAIT_TIME | BIGINT | Deprecated. Displays the wait time between two sampling runs, in milliseconds (SAMPLING_INTERVAL) |
| MEMORY_LIMIT | BIGINT | Displays the limit for profiling data in bytes. This is not an exact limit, a heuristic approach is used to limit memory. |
| SAMPLING_INTERVAL | BIGINT | Displays the sampling interval, in milliseconds. |
| CONNECTION_ID | INTEGER | Displays the connection ID to filter on. |
| ROOT_STATEMENT_HASH | NVARCHAR(32) | Displays the root statement hash to filter on. |
| TRACEPROFILE_NAME | NVARCHAR(128) | Displays the userspecific trace profile name to filter on. |
| START_TIME | TIMESTAMP | Displays the time that profiling was started. |
| STOP_TIME | TIMESTAMP | Displays the time that profiling was stopped. |
| MEMORY_SIZE | BIGINT | Displays the current size, in bytes, of the kernel profile. |
| SAMPLE_COUNT | BIGINT | Displays the number of samples stored for the profile. |
| STATUS |   | Displays the status of the profiler. Possible values are: STARTED, STOPPED |

## Related Information

[ALTER SYSTEM {START | STOP | SAVE | CLEAR} KERNEL PROFILER Statement (System Management)](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-START-STOP-SAVE-CLEAR-KERNEL-PROFILER.md)
