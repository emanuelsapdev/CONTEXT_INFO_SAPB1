# 6.2.130 M_HOST_RESOURCE_UTILIZATION System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1822–1824

Provides information about host resource utilization by all processes (including non-SAP HANA processes). CPU time is in milliseconds and added across all cores since system start.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| FREE_PHYSICAL_MEMORY | BIGINT | Displays the free physical memory on the host in bytes. |
| USED_PHYSICAL_MEMORY | BIGINT | Displays the used physical memory on the host in bytes. |
| FREE_SWAP_SPACE | BIGINT | Displays the free swap memory on the host in bytes. |
| USED_SWAP_SPACE | BIGINT | Displays the used swap memory on the host in bytes. |
| ALLOCATION_LIMIT | BIGINT | Displays the allocation limit for all processes in bytes. |
| INSTANCE_TOTAL_MEMORY_USED_SIZE | BIGINT | Displays the amount of memory from the memory pool that is currently being used by SAP HANA processes in bytes. |
| INSTANCE_TOTAL_MEMORY_PEAK_USED_SIZE | BIGINT | Displays the peak memory from the memory pool used by SAP HANA processes since the instance started (this is a sample-based value) in bytes. |
| INSTANCE_TOTAL_MEMORY_ALLOCATED_SIZE | BIGINT | Displays the size of the memory pool for all SAP HANA processes in bytes. |
| INSTANCE_CODE_SIZE | BIGINT | Displays the code size, including shared libraries of SAP HANA processes in bytes. |
| INSTANCE_SHARED_MEMORY_ALLOCATED_SIZE | BIGINT | Displays the shared memory size of SAP HANA processes in bytes. |
| TOTAL_CPU_USER_TIME | BIGINT | Displays the CPU time spent in the user mode in milliseconds. |
| TOTAL_CPU_SYSTEM_TIME | BIGINT | Displays the CPU time spent in the kernel mode in milliseconds. |
| TOTAL_CPU_WIO_TIME | BIGINT | Displays the CPU time spent in wait I/O in milliseconds. Linux only, Microsoft Windows is always 0. |
| TOTAL_CPU_IDLE_TIME | BIGINT | Displays the CPU idle time in milliseconds. |
| SYS_TIMESTAMP | TIMESTAMP | Displays the host timestamp in the local time zone. |
| UTC_TIMESTAMP | TIMESTAMP | Displays the host timestamp in UTC. |
| OPEN_FILE_COUNT | BIGINT | Displays the number of allocated file handles on the host. The Kernel parameter is `fs.file-nr`. For more information, see the OPEN_FILE_LIMIT key in the M_HOST_INFORMATION system view topic. |
| ACTIVE_ASYNC_IO_COUNT | BIGINT | Displays the number of asynchronous input and/or output requests on the host. The Kernel parameter is `fs.ai-` `nr`. For more information, see the ASYNC_IO_LIMIT key in the M_HOST_INFORMATION system view topic. |

## Related Information

M_HOST_INFORMATION System View [→](M_HOST_INFORMATION-System-View.md) M_HOST_NETWORK_STATISTICS System View [→](M_HOST_NETWORK_STATISTICS-System-View.md)
