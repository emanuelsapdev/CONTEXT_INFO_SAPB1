# 6.2.156 M_LIVECACHE_PROCEDURE_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1859–1870

Provides accumulated LiveCache procedure statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| OBJECT_NAME | VARCHAR(128) | Displays the object name. |
| METHOD_NAME | VARCHAR(128) | Displays the method name. |
| CALL_COUNT | BIGINT | Displays the number of calls of the procedure. |
| SUM_RUN_TIME | BIGINT | Displays the total runtime of the procedure in microseconds. |
| MAX_RUN_TIME | BIGINT | Displays the maximum runtime of the procedure in microseconds. |
| MIN_RUN_TIME | BIGINT | Displays the minimum runtime of the procedure in microseconds. |
| AVERAGE_RUN_TIME | BIGINT | Displays the average runtime of the procedure in microseconds. |
| DEREF_COUNT | BIGINT | Displays the number of OID derefs. |
| DEREF_BASE_COUNT | BIGINT | Displays the number of OID derefs against basis. |
| DEREF_BASE_IN_VERSION_COUNT | BIGINT | Displays the number of OID derefs against basis from within an OMS version. |
| DEREF_KEYED_OBJECT_COUNT | BIGINT | Displays the number of key derefs. |
| DEREF_KEYED_OBJECT_BASE_COUNT | BIGINT | Displays the number of key derefs against basis. |
| DEREF_KEYED_OBJECT_BASE_IN_VERSION_COUNT | BIGINT | Displays the number of key derefs against basis from within an OMS version. |
| ITER_BASE_COUNT | BIGINT | Displays the number of objects read via an OID-iterator from the basis. |
| ITER_KEYED_OBJECT_BASE_COUNT | BIGINT | Displays the number of objects read via a key-iterator from the basis. |
| ITER_BASE_IN_VERSION_COUNT | BIGINT | Displays the number of objects read via an OID-iterator from the basis from within an OMS version. |
| ITER_IN_VERSION_COUNT | BIGINT | Displays the number of objects, created in an OMS-version, read via an OID-iterator . |
| ITER_KEYED_OBJECT_BASE_IN_VERSION_COUNT | BIGINT | Displays the number of objects read via an OID-iterator from the basis from within an OMS version. |
| ITER_KEYED_OBJECT_IN_VERSION_COUNT | BIGINT | Displays the number of objects, created in an OMS version, read via a key-iterator. |
| DEREF_VAR_OBJECT_COUNT | BIGINT | Displays the number of derefs of var objects. |
| DEREF_VAR_OBJECT_BASE_COUNT | BIGINT | Displays the number of derefs of var objects against basis. |
| DEREF_VAR_OBJECT_BASE_SIZE | BIGINT | Displays the accumulated size of var objects read from the basis in bytes. |
| DEREF_VAR_OBJECT_BASE_IN_VERSION_COUNT | BIGINT | Displays the number of derefs of var objects against basis from within an OMS version. |
| DEREF_VAR_OBJECT_BASE_IN_VERSION_SIZE | BIGINT | Displays the accumulated size of var objects read from the basis from within an OMS version in bytes. |
| NEW_OBJECT_COUNT | BIGINT | Displays the number of newly created standard objects. |
| NEW_KEYED_OBJECT_COUNT | BIGINT | Displays the number of newly created keyed objects. |
| NEW_VAR_OBJECT_COUNT | BIGINT | Displays the number of newly created var objects. |
| NEW_OBJECT_IN_VERSION_COUNT | BIGINT | Displays the number of newly created standard objects in an OMS version. |
| NEW_KEYED_OBJECT_IN_VERSION_COUNT | BIGINT | Displays the number of newly created keyed objects in an OMS version. |
| NEW_VAR_OBJECT_IN_VERSION_COUNT | BIGINT | Displays the number of newly created var objects in an OMS version. |
| STORE_COUNT | BIGINT | Displays the number of store calls on standard objects. |
| STORE_IN_VERSION_COUNT | BIGINT | Displays the number of store calls on standard objects in an OMS version. |
| STORE_KEYED_OBJECT_COUNT | BIGINT | Displays the number of store calls on keyed objects. |
| STORE_KEYED_OBJECT_IN_VERSION_COUNT | BIGINT | Displays the number of store calls on keyed objects in an OMS version. |
| STORE_VAR_OBJECT_COUNT | BIGINT | Displays the number of store calls on var objects. |
| STORE_VAR_OBJECT_SIZE | BIGINT | Displays the accumulated size of store calls on var objects in bytes. |
| STORE_VAR_OBJECT_IN_VERSION_COUNT | BIGINT | Displays the number of store calls on var objects in an OMS version. |
| STORE_VAR_OBJECT_IN_VERSION_SIZE | BIGINT | Displays the accumulated size of store calls on var objects in an OMS version in bytes. |
| STORE_BASE_COUNT | BIGINT | Displays the number of updates of standard objects in the basis. |
| STORE_KEYED_OBJECT_BASE_COUNT | BIGINT | Displays the number of updates of keyed objects in the basis. |
| STORE_VAR_OBJECT_BASE_COUNT | BIGINT | Displays the number of updates of var objects in the basis. |
| STORE_VAR_OBJECT_BASE_SIZE | BIGINT | Displays the accumulated sizes of updated objects in the basis in bytes. |
| DELETE_COUNT | BIGINT | Displays the number of delete calls on standard objects. |
| DELETE_KEYED_OBJECT_COUNT | BIGINT | Displays the number of delete calls on keyed objects. |
| DELETE_VAR_OBJECT_COUNT | BIGINT | Displays the number of delete calls on var objects. |
| DELETE_IN_VERSION_COUNT | BIGINT | Displays the number of delete calls on standard objects in an OMS version. |
| DELETE_KEYED_OBJECT_IN_VERSION_COUNT | BIGINT | Displays the number of delete calls on keyed objects in an OMS version. |
| DELETE_VAR_OBJECT_IN_VERSION_COUNT | BIGINT | Displays the number of delete calls on var objects in an OMS version. |
| DELETE_BASE_COUNT | BIGINT | Displays the number of deleted standard objects in the basis. |
| DELETE_KEYED_OBJECT_BASE_COUNT | BIGINT | Displays the number of deleted keyed objects in the basis. |
| DELETE_VAR_OBJECT_BASE_COUNT | BIGINT | Displays the number of deleted var objects in the basis. |
| LOCK_EXCLUSIVE_BASE_COUNT | BIGINT | Displays the number of exclusive lock requests on standard objects in the basis. |
| LOCK_SHARE_BASE_COUNT | BIGINT | Displays the number of share lock requests on standard objects in the basis. |
| LOCK_EXCLUSIVE_KEYED_OBJECT_BASE_COUNT | BIGINT | Displays the number of exclusive lock requests on keyed objects in the basis. |
| LOCK_SHARE_KEYED_OBJECT_BASE_COUNT | BIGINT | Displays the number of share lock requests on keyed objects in the basis. |
| LOCK_EXCLUSIVE_VAR_OBJECT_BASE_COUNT | BIGINT | Displays the number of exclusive lock requests on var objects in the basis. |
| LOCK_SHARE_VAR_OBJECT_BASE_COUNT | BIGINT | Displays the nNumber of share lock requests on var objects in the basis. |
| RELEASE_CALLED_COUNT | BIGINT | Displays the number of OMS release calls. |
| RELEASE_EXECUTED_COUNT | BIGINT | Displays the number of released standard objects. |
| RELEASE_EXECUTED_KEYED_OBJECT_COUNT | BIGINT | Displays the number of releases keyed objects. |
| RELEASE_EXECUTED_VAR_OBJECT_COUNT | BIGINT | Displays the number of releases var objects. |
| HISTORY_HOP_COUNT | BIGINT | Displays the number of hops in the history chain during deref. |
| ITER_HISTORY_HOP_COUNT | BIGINT | Displays the number of hops in the history chain during iteration. |
| EXCEPTION_COUNT | BIGINT | Displays the number of dbp-exceptions thrown. |
| OUT_OF_DATE_EXCEPTION_COUNT | BIGINT | Displays the number of out-of-date-exceptions thrown. |
| OUT_OF_MEMORY_EXCEPTION_COUNT | BIGINT | Displays the number of out-of-memory-exceptions thrown. |
| TIMEOUT_EXCEPTION_COUNT | BIGINT | Displays the number of timeout-exceptions thrown. |
| OMS_TERMINATE_COUNT | BIGINT | Displays the number of OMS terminate calls. |
| SUBTRANSACTION_ROLLBACK_COUNT | BIGINT | Displays the number of rolled back sub-transactions. |
| SUBTRANSACTION_COMMIT_COUNT | BIGINT | Displays the number of committed sub-transactions. |
| MAX_SUBTRANSACTION_LEVEL | BIGINT | Displays the maximum subtransaction level. |
| NEW_CONSISTENT_VIEW_COUNT | BIGINT | Displays the number of new-consistent-view calls with objects. |
| SUM_NEW_CONSISTENT_VIEW_WAIT_TIME | BIGINT | Displays the sum of the wait times of the new-consistent-view calls with objects. |
| AVERAGE_NEW_CONSISTENT_VIEW_WAIT_TIME | BIGINT | Displays the average wait time of new-consistent-view calls with objects in seconds. |
| NEW_CONSISTENT_VIEW_MAX_WAIT_TIME | BIGINT | Displays the maximal wait time of new-consistent-view calls with objects in seconds. |
| KEY_CACHE_HIT_COUNT | BIGINT | Displays the number of cache hits in the key-cache. |
| KEY_MISS_CACHE_HIT_COUNT | BIGINT | Displays the number of cache hits in the key-miss-cache. |
| DEREF_VERSION_KEYED_OBJECT_COUNT | BIGINT | Displays the number of key-derefs in an OMS version on objects created in this version. |
| OMS_REHASH_COUNT | BIGINT | Displays the number of rehashes of the OMS-object-hash. |
| AVERAGE_HASH_CHAIN_SEARCH_LENGTH | BIGINT | Displays the average search length on the hash-chains, in microseconds, of the OMS-object-hash. |
| MAX_HASH_CHAIN_LENGTH | BIGINT | Displays the maximum length of a hash-chain of the OMS-object-hash. |
| VERSION_CREATE_COUNT | BIGINT | Displays the number of created OMS versions. |
| VERSION_OPEN_COUNT | BIGINT | Displays the number of open-version calls. |
| VERSION_CLOSE_COUNT | BIGINT | Displays the number of close-version calls. |
| VERSION_DROP_COUNT | BIGINT | Displays the number of dropped OMS versions. |
| USER_ALLOC_COUNT | BIGINT | Displays the number of allocations via a user allocator. |
| USER_MAX_CHUNK_ALLOCATED_SIZE | BIGINT | Displays the maximum size of a chunk allocated via a user allocator in bytes. |
| USER_MIN_CHUNK_ALLOCATED_SIZE | BIGINT | Displays the minimum size of a chunk allocated via a user allocator in bytes. |
| USER_AVERAGE_CHUNK_ALLOCATED_SIZE | BIGINT | Displays the average size of a chunk allocated via a user allocator in bytes. |
| USER_DELETE_COUNT | BIGINT | Displays the number of deallocations via a user allocator. |
| USER_MAX_CHUNK_DELETED_SIZE | BIGINT | Displays the maximum size of a chunk deallocated via a user allocator in bytes. |
| USER_MIN_CHUNK_DELETED_SIZE | BIGINT | Displays the minimum size of a chunk deallocated via a user allocator in bytes. |
| USER_AVERAGE_CHUNK_DELETED_SIZE | BIGINT | Displays the average size of a chunk deallocated via a user allocator in bytes. |
| USER_DELTA_MAX_SIZE | BIGINT | Displays the maximal difference in size between allocation and deallocation on a user allocator during the execution of a method in bytes. |
| OMS_ALLOC_COUNT | BIGINT | Displays the number of allocations via an OMS internal allocator. |
| OMS_MAX_CHUNK_ALLOCATED_SIZE | BIGINT | Displays the maximum size of a chunk allocated via an OMS internal allocator in bytes. |
| OMS_MIN_CHUNK_ALLOCATED_SIZE | BIGINT | Displays the minimum size of a chunk allocated via an OMS internal allocator in bytes. |
| OMS_AVERAGE_CHUNK_ALLOCATED_SIZE | BIGINT | Displays the average size of a chunk allocated via an OMS internal allocator in bytes. |
| OMS_DELETE_COUNT | BIGINT | Displays the number of deallocations via an OMS internal allocator. |
| OMS_MAX_CHUNK_DELETED_SIZE | BIGINT | Displays the maximum size of a chunk deallocated via an OMS internal allocator in bytes. |
| OMS_MIN_CHUNK_DELETED_SIZE | BIGINT | Displays the minimum size of a chunk deallocated via an OMS internal allocator in bytes. |
| OMS_AVERAGE_CHUNK_DELETED_SIZE | BIGINT | Displays the average size of a chunk deallocated via an OMS internal allocator in bytes. |
| OMS_DELTA_MAX_SIZE | BIGINT | Displays the maximum difference in size between allocation and deallocation on an OMS internal allocator during the execution of a method in bytes. |
| LAST_USER_DELTA_MAX_SIZE | BIGINT | Displays the last peak delta of the user heap consumption during procedure execution in bytes. |
| MAX_USER_DELTA_MAX_SIZE | BIGINT | Displays the maximum peak delta of the user heap consumption during procedure execution in bytes. |
| MIN_USER_DELTA_MAX_SIZE | BIGINT | Displays the minimum peak delta of the user heap consumption during procedure execution in bytes. |
| SUM_USER_DELTA_MAX_SIZE | BIGINT | Displays the total peak delta of the user heap consumption during procedure execution in bytes. |
| AVG_USER_DELTA_MAX_SIZE | BIGINT | Displays the peak delta of the user heap consumption during procedure execution in bytes. |
| LAST_OMS_DELTA_SIZE | BIGINT | Displays the last delta of the OMS heap consumption between start and end of the procedure execution in bytes. |
| MAX_OMS_DELTA_SIZE | BIGINT | Displays the maximum delta of the OMS heap consumption between the start and end of the procedure execution in bytes. |
| MIN_OMS_DELTA_SIZE | BIGINT | Displays the minimum delta of the OMS heap consumption between the start and end of the procedure execution in bytes. |
| SUM_OMS_DELTA_SIZE | BIGINT | Displays the total delta of the OMS heap consumption between the start and end of the procedure execution in bytes. |
| AVG_OMS_DELTA_SIZE | BIGINT | Displays the average delta of the OMS heap consumption between the start and end of the procedure execution in bytes. |
| LAST_VERSION_DELTA_SIZE | BIGINT | Displays the last delta of the OMS version heap consumption between the start and end of the procedure execution in bytes. |
| MAX_VERSION_DELTA_SIZE | BIGINT | Displays the maximum delta of the OMS version heap consumption between the start and end of the procedure execution in bytes. |
| MIN_VERSION_DELTA_SIZE | BIGINT | Displays the minimum delta of the OMS version heap consumption between the start and end of the procedure execution in bytes. |
| SUM_VERSION_DELTA_SIZE | BIGINT | Displays the total delta of the OMS version heap consumption between the start and end of the procedure execution in bytes. |
| AVG_VERSION_DELTA_SIZE | BIGINT | Displays the average delta of the OMS version heap consumption between the start and end of the procedure execution in bytes. |
| LAST_HEAP_DELTA_SIZE | BIGINT | Displays the last delta of the overall heap consumption (user + OMS + OMS version) between the start and end of the procedure execution. |
| MAX_HEAP_DELTA_SIZE | BIGINT | Displays the maximum delta of the overall heap consumption (user + OMS + OMS version) between the start and end of the procedure execution in bytes. |
| MIN_HEAP_DELTA_SIZE | BIGINT | Displays the minimum delta of the over all heap consumption (user + OMS + OMS version) between the start and end of the procedure execution in bytes. |
| SUM_HEAP_DELTA_SIZE | BIGINT | Displays the total delta of the overall heap consumption (user + OMS + OMS version) between the start and end of the procedure execution in bytes. |
| AVG_HEAP_DELTA_SIZE | BIGINT | Displays the average delta of the overall heap consumption (user + OMS + OMS version) between the start and end of the procedure execution in bytes. |
| STREAM_COMMUNICATION_TIME | BIGINT | Displays the total stream communication time in microseconds. |
| MAX_STREAM_COMMUNICATION_TIME | BIGINT | Displays the maximum stream communication time in microseconds. |
| MIN_STREAM_COMMUNICATION_TIME | BIGINT | Displays the minimum stream communication time in microseconds. |
| AVG_STREAM_COMMUNICATION_TIME | BIGINT | Displays the average stream communication time in microseconds. |
| STREAM_READ_COUNT | BIGINT | Displays the number of communications for reading ABAP tables. |
| STREAM_WRITE_COUNT | BIGINT | Displays the number of communications for writing ABAP tables. |
| STREAM_READ_ROW_COUNT | BIGINT | Displays the number of rows read from ABAP tables. |
| STREAM_WRITE_ROW_COUNT | BIGINT | Displays the number of rows written to ABAP tables. |
| LAST_INTERNAL_SQL_PREPARE_TIME | BIGINT | Displays last the internal SQL prepare time. |
| MAX_INTERNAL_SQL_PREPARE_TIME | BIGINT | Displays the maximum internal SQL prepare time. |
| MIN_INTERNAL_SQL_PREPARE_TIME | BIGINT | Displays the minimum internal SQL prepare time. |
| SUM_INTERNAL_SQL_PREPARE_TIME | BIGINT | Displays the total internal SQL prepare time. |
| AVG_INTERNAL_SQL_PREPARE_TIME | BIGINT | Displays the average internal SQL prepare time. |
| LAST_INTERNAL_SQL_EXECUTE_TIME | BIGINT | Displays the last internal SQL execute time. |
| MAX_INTERNAL_SQL_EXECUTE_TIME | BIGINT | Displays the maximum internal SQL execute time. |
| MIN_INTERNAL_SQL_EXECUTE_TIME | BIGINT | Displays the minimum internal SQL execute time. |
| SUM_INTERNAL_SQL_EXECUTE_TIME | BIGINT | Displays the total internal SQL execute time. |
| AVG_INTERNAL_SQL_EXECUTE_TIME | BIGINT | Displays the average internal SQL execute time. |
| LAST_INTERNAL_SQL_FETCH_TIME | BIGINT | Displays the last internal SQL fetch time. |
| MAX_INTERNAL_SQL_FETCH_TIME | BIGINT | Displays the maximum internal SQL fetch time. |
| MIN_INTERNAL_SQL_FETCH_TIME | BIGINT | Displays the minimum internal SQL fetch time. |
| SUM_INTERNAL_SQL_FETCH_TIME | BIGINT | Displays the total internal SQL fetch time. |
| AVG_INTERNAL_SQL_FETCH_TIME | BIGINT | Displays the avg internal SQL fetch time. |

## Additional Information

This view can only be used if liveCache is enabled.

For each liveCache procedure, which has been called already since the last restart, statistics are shown.

This view has a resettable counterpart; you can see the values since the last reset in the M_LIVECACHE_PROCEDURE_STATISTICS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_LIVECACHE_PROCEDURE_STATISTICS_RESET;`.

## Related Information

M_LIVECACHE_PROCEDURE_STATISTICS_RESET System View [→](M_LIVECACHE_PROCEDURE_STATISTICS_RESET-System-View.md) ALTER SYSTEM RESET MONITORING VIEW Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RESET-MONITORING-VIEW-Statement-System.md)
