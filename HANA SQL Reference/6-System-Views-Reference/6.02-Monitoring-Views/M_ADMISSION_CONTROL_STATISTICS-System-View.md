# 6.2.7 M_ADMISSION_CONTROL_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1646–1647

Provides the overall statistics values of the Session-Wise Admission Control feature.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| TOTAL_ADMIT_COUNT | BIGINT | Displays the accumulated request admission count. |
| TOTAL_REJECT_COUNT | BIGINT | Displays the accumulated request rejection count. |
| TOTAL_ENQUEUE_COUNT | BIGINT | Displays the accumulated request queued count. |
| TOTAL_DEQUEUE_COUNT | BIGINT | Displays the accumulated request dequeued count (the executed request count). |
| TOTAL_TIMEOUT_COUNT | BIGINT | Displays the accumulated request dequeued count due to timeout (the rejected request count). |
| CURRENT_QUEUE_SIZE | BIGINT | Displays the current waiting request queued count. |
| LAST_CPU_USAGE_RATIO | INTEGER | Displays the last measured value of the CPU us age. |
| LAST_CPU_USAGE_MEASURE_TIME | TIMESTAMP | Displays the time at which the last CPU usage ratio was measured. |
| LAST_MEMORY_SIZE | BIGINT | Displays the last measured memory size in GB. |
| LAST_MEMORY_RATIO | BIGINT | Displays the last measured memory size, as a percentage of the global allocation limit (last_mem ory_size/memory_allocation_limit). |
| LAST_MEMORY_MEASURE_TIME | TIMESTAMP | Displays the time at which the last memory size was measured. |
| LAST_WAIT_TIME | BIGINT | Displays the last wait time of the request in the queue in microseconds. |
| AVG_WAIT_TIME | BIGINT | Displays the average wait time of the request in the queue in microseconds. |
| MAX_WAIT_TIME | BIGINT | Displays the maximum wait time of the request in the queue in microseconds. |
| MIN_WAIT_TIME | BIGINT | Displays the minimum wait time of the request in the queue in microseconds. |
| SUM_WAIT_TIME | BIGINT | Displays the total wait time of the request in the queue in microseconds. |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |

## Related Information

M_ADMISSION_CONTROL_EVENTS System View [→](M_ADMISSION_CONTROL_EVENTS-System-View.md) M_ADMISSION_CONTROL_QUEUES System View [→](M_ADMISSION_CONTROL_QUEUES-System-View.md)
