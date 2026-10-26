# 6.2.136 M_JOBEXECUTORS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1830–1832

Provides job executor statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| MAX_CONCURRENCY | INTEGER | Displays the maximum number of con currently running worker threads.<br>The job executor keeps MAX_CONCURRENCY worker threads busy. As a result, more worker threads are started if some worker threads are in a wait state for some time. Even if these additional worker threads are terminated, some of them are kept for later use and counted in PARKED_WORKER_COUNT. |
| TOTAL_WORKER_COUNT | INTEGER | Displays the total number of worker threads, including one extra worker thread for emergency diagnostic purposes. |
| PARKED_WORKER_COUNT | INTEGER | Displays the number of parked worker threads. |
| FREE_WORKER_COUNT | INTEGER | Displays the total number of worker threads that are idle and may immediately take up a job to work on. |
| SYS_WAITING_WORKER_COUNT | INTEGER | Displays the number of worker threads waiting in system. A worker thread may wait for any other kind of synchronization. |
| JOB_WAITING_WORKER_COUNT | INTEGER | Displays the number of worker threads waiting for a job on another worker thread. |
| YIELD_WAITING_WORKER_COUNT | INTEGER | Displays the number of worker threads waiting on a yield. Sometimes a job running on a worker thread yields execution to another job that is more important. |
| TOTAL_WAITING_JOB_COUNT | BIGINT | Displays the number of all jobs waiting for execution. |
| QUEUED_WAITING_JOB_COUNT | BIGINT | Displays the number of jobs queued for execution. |
| WORKER_CREATE_COUNT | BIGINT | Displays the number of threads created. |

## Additional Information

This view has a resettable counterpart; you can see the values since the last reset in the M_JOBEXECUTORS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_JOBEXECUTORS_RESET;`.

## Related Information

[M_JOBEXECUTORS_RESET System View](M_JOBEXECUTORS_RESET-System-View.md)
