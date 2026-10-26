# 6.2.260 M_SERVICE_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1997–1999

Provides statistics on active services.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SERVICE_NAME | VARCHAR(32) | Displays the service name. |
| PROCESS_ID | INTEGER | Displays the process ID. |
| DETAIL | VARCHAR(128) | Displays the detail information, similar to COORDINATOR_TYPE in M_SERVICES. |
| ACTIVE_STATUS | VARCHAR(16) | Displays the active status. This column contains the following values:<br>• NO - Displays that the service has not started.<br>• YES - Displays that the service has started and is ready for requests.<br>• UNKNOWN - Displays the initial state after starting a landscape, or when the state is not known (for example, after a crash). If the service does not start within a minute, this state changes to NO.<br>• STARTING - Displays that the service is starting. This state might last for several minutes on first startup or recovery.<br>• STOPPING - Displays that the service is stopping. |
| START_TIME | TIMESTAMP | Displays the process start timestamp. |
| SYS_TIMESTAMP | TIMESTAMP | Displays the current system timestamp. |
| PROCESS_CPU | SMALLINT | Displays the CPU usage percentage of the current process. See additional notes after this table. |
| PROCESS_CPU_TIME | BIGINT | Displays the CPU usage of the current process since the start in milliseconds. |
| TOTAL_CPU | SMALLINT | Displays the CPU usage percentage of all processes. See additional notes after this table. |
| TOTAL_CPU_TIME | BIGINT | Displays the CPU usage of all processes since the start in milliseconds. See additional notes after this table. |
| PROCESS_MEMORY | BIGINT | Displays the process logical memory usage in bytes. |
| PROCESS_PHYSICAL_MEMORY | BIGINT | Displays the process physical memory usage in bytes. |
| TOTAL_MEMORY | BIGINT | Displays the host physical and swap memory usage in bytes. |
| AVAILABLE_MEMORY | BIGINT | Displays the host physical and swap memory size in bytes. |
| PHYSICAL_MEMORY | BIGINT | Displays the host physical memory size in bytes. |
| REQUESTS_PER_SEC | DOUBLE | Displays the requests per second. For internal use only. |
| RESPONSE_TIME | INTEGER | Displays the response time in milliseconds. For internal use only. |
| FINISHED_NON_INTERNAL_REQUEST_COUNT | BIGINT | Displays the number of finished requests. For internal use only. |
| ALL_FINISHED_REQUEST_COUNT | BIGINT | Displays the finished requests, including internal requests. For internal use only. |
| ACTIVE_REQUEST_COUNT | INTEGER | Displays the number of active requests. For internal use only. |
| PENDING_REQUEST_COUNT | INTEGER | Displays the number of pending requests. For internal use only. |
| ACTIVE_THREAD_COUNT | INTEGER | Displays the number of active threads. |
| THREAD_COUNT | INTEGER | Displays the number of total threads. |
| OPEN_FILE_COUNT | INTEGER | Displays the number of open files. |

## Additional Information

#### PROCESS_CPU , TOTAL_CPU

PROCESS_CPU and TOTAL_CPU contain CPU usage in percent since last select. This select could be done by another user or another session.

To calculate exact CPU usage use 2 selects and this formula:

```sql
process_cpu = (select2.process_cpu-time - select1.process_cpu_time) /
(select2.sys_timestamp - select1.sys_timestamp)
  total_cpu   = (select2.total_cpu_time   - select1.total_cpu_time  ) /
(select2.sys_timestamp - select1.sys_timestamp)
```

**TOTAL_CPU_TIME** TOTAL_CPU_TIME counts the CPU usage as if there would be 1 core. M_HOST_RESOURCE_UTILIZATION shows similar values multiplied by the number of cores.

```sql
select s.host,s.total_cpu_time,(h.total_cpu_user_time
+h.total_cpu_system_time)/i.value
from m_service_statistics s, m_host_resource_utilization h,
m_host_information i
where s.service_name='nameserver' and i.key='cpu_threads'and s.host=h.host
and s.host=i.host
```

## Related Information

[M_HOST_RESOURCE_UTILIZATION System View](M_HOST_RESOURCE_UTILIZATION-System-View.md)
