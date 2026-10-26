# 6.2.41 M_COMPACTION_THREAD System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1680–1683

Provides compaction thread statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| NUM_COMPACTION_COLLISIONS | BIGINT | Displays the count of memory compaction collisions, which includes other threads currently in compaction and unforced compactions. |
| NUM_COMPACTIONS | BIGINT | Displays the number of compaction requests. |
| LAST_SIZE_COMPACTION_REQUESTS | BIGINT | Displays the size in bytes of the last compaction request. |
| MAX_SIZE_COMPACTION_REQUESTS | BIGINT | Displays the maximum sized compaction request in bytes. |
| MIN_SIZE_COMPACTION_REQUESTS | BIGINT | Displays the minimum sized compaction request in bytes. |
| SUM_SIZE_COMPACTION_REQUESTS | BIGINT | Displays the total size of compaction requests in bytes. |
| AVG_SIZE_COMPACTION_REQUESTS | BIGINT | Displays the average size of compaction requests in bytes. |
| LAST_SIZE_FREEABLE | BIGINT | Displays the size in bytes compacted by the last at compaction call. |
| MAX_SIZE_FREEABLE | BIGINT | Displays the size in bytes compacted by the maximum compaction call. |
| MIN_SIZE_FREEABLE | BIGINT | Displays the size in bytes compacted by the minimum compaction call. |
| SUM_SIZE_FREEABLE | BIGINT | Displays the size in bytes compacted by all compaction calls (total). |
| AVG_SIZE_FREEABLE | BIGINT | Displays the size in bytes compacted by the average compaction call. |
| LAST_SIZE_FREED_BY_GARBAGE_COLLECTION | BIGINT | Displays the size in bytes compacted by the last memory garbage collection (defragmentation). |
| MAX_SIZE_FREED_BY_GARBAGE_COLLECTION | BIGINT | Displays the size in bytes compacted by the largest memory garbage collection (defragmentation). |
| MIN_SIZE_FREED_BY_GARBAGE_COLLECTION | BIGINT | Displays the size in bytes compacted by the smallest memory garbage collection (defragmentation). |
| SUM_SIZE_FREED_BY_GARBAGE_COLLECTION | BIGINT | Displays the size in bytes compacted by all memory garbage collections (defragmentation) (total). |
| AVG_SIZE_FREED_BY_GARBAGE_COLLECTION | BIGINT | Displays the size in bytes compacted by the average memory garbage collection (defragmentation). |
| LAST_COMPACTION_RESULT | BIGINT | Displays the last compaction result in bytes. This is the difference of allocated bytes before and after compaction and may be influenced by other factors than compaction. |
| MAX_COMPACTION_RESULT | BIGINT | Displays the largest compaction result in bytes. This is the difference of allocated bytes before and after compaction and may be influenced by other factors than compaction. |
| MIN_COMPACTION_RESULT | BIGINT | Displays the smallest compaction result in bytes. This is the difference of allocated bytes before and after compaction and may be influenced by other factors than compaction. |
| SUM_COMPACTION_RESULT | BIGINT | Displays the total of all compaction results in bytes. This is the difference of allocated bytes before and after compaction and may be influenced by other factors than compaction. |
| AVG_COMPACTION_RESULT | BIGINT | Displays the average compaction result in bytes. This is the difference of allocated bytes before and after compaction and may be influenced by other factors than compaction. |

## Additional Information

The compaction thread automatically calls for memory reduction (including for the resource container) if memory gets low, but is not already exhausted. The compaction thread also executes the memory reduction requests triggered by other processes (inter-process memory management). This view displays some information about the compaction requests and the compacted sizes.
