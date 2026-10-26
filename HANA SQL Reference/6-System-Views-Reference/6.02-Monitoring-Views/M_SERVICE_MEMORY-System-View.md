# 6.2.254 M_SERVICE_MEMORY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1988–1990

Displays detailed memory utilization information by services.

## Structure

| **Column name** | **Data type** | **Unit** | **Description** |
| --- | --- | --- | --- |
| HOST | VARCHAR(64) |   | Displays the host name. |
| PORT | INTEGER |   | Displays the internal port. |
| SERVICE_NAME | VARCHAR(32) |   | Displays the service name. |
| PROCESS_ID | INTEGER |   | Displays the process ID. |
| LOGICAL_MEMORY_SIZE | BIGINT | Byte | Displays the virtual memory size, in bytes, from the operating system perspective. |
| PHYSICAL_MEMORY_SIZE | BIGINT | Byte | Displays the physical resident memory size, in bytes, from the operating system perspective. |
| CODE_SIZE | BIGINT | Byte | Displays the code size, including shared libraries in bytes. |
| STACK_SIZE | BIGINT | Byte | Displays the stack size in bytes. |
| HEAP_MEMORY_ALLOCATED_SIZE | BIGINT | Byte | Displays the heap part of the memory pool. |
| HEAP_MEMORY_USED_SIZE | BIGINT | Byte | Displays the amount of pool heap memory that is in use in bytes. |
| SHARED_MEMORY_ALLOCATED_SIZE | BIGINT | Byte | Displays the shared memory part of the memory pool in bytes. |
| SHARED_MEMORY_USED_SIZE | BIGINT | Byte | Displays the amount of pool shared memory that is in use in bytes. |
| COMPACTORS_ALLOCATED_SIZE | BIGINT | Byte | Displays the part of the memory pool that can potentially (if unpinned) be freed during a memory shortage in bytes. |
| COMPACTORS_FREEABLE_SIZE | BIGINT | Byte | Displays the memory that can be freed during a memory shortage in bytes. |

| BIGINT | Byte | Displays the maximum memory pool size in bytes (config urable value). |
| --- | --- | --- |

ALLOCATION_LIMIT

| EFFECTIVE_ALLOCATION_LIMIT | BIGINT | Byte | Displays the effective maximum memory pool size, in bytes, considering the pool sizes of other processes (computed value). |
| --- | --- | --- | --- |

| **Column name** | **Data type** | **Unit** | **Description** |
| --- | --- | --- | --- |
| BLOCKED_MEMORY_LIMIT | BIGINT | Byte | Displays the minimum guaranteed memory for the proc ess in bytes. |
| FREE_MEMORY_SIZE | BIGINT | Byte | Displays the allocated free memory in bytes. |
| MIN_SEGMENT_SIZE | BIGINT | Byte | Displays the minimum segment size for getting heap memory from the operating system in bytes. |
| VIRTUAL_ADDRESS_SPACE_USED_SIZE | BIGINT | Byte | Displays the used size of the virtual address space in bytes. |
| VIRTUAL_ADDRESS_SPACE_TOTAL_SIZE | BIGINT | Byte | Displays the total virtual address space for each process in bytes. |
| FRAGMENTED_MEMORY_SIZE | BIGINT | Byte | Displays the amount of memory held by SAP HANA memory management in bytes. This memory cannot be easily reused for new memory allocations. |
| TOTAL_MEMORY_USED_SIZE | BIGINT |   | Displays the amount of memory in use from the memory pool in bytes. |
