# 6.2.111 M_EXPENSIVE_STATEMENT_EXECUTION_LOCATION_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1796–1797

Provides location statistics for expensive statements.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| STATEMENT_EXECUTION_ID | BIGINT | Displays the execution ID of the statement. |
| START_TIME | TIMESTAMP | Displays the execution start time of the statement. |
| EXECUTION_HOST | VARCHAR(64) | Displays the host where the statement was executed. |
| EXECUTION_PORT | INTEGER | Displays the port of the host where the statement was executed. |
| MEMORY_SIZE | BIGINT | Displays the peak memory usage for the host in bytes. For example, if host A has a peak usage of 2 GB and host B has a peak usage of 3 GB, then there is a row with host A showing 2 GB and a row with host B showing 3 GB. |
| CPU_TIME | BIGINT | Displays the tracked CPU time that each location consumed. |

## Related Information

[M_EXPENSIVE_STATEMENTS System View](M_EXPENSIVE_STATEMENTS-System-View.md)
