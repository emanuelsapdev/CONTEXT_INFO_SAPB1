# 6.2.153 M_LIVECACHE_LOCK_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1856–1857

Provides accumulated LiveCache lock statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| CONTAINER_EXCLUSIVE_COUNT | BIGINT | Displays the number of exclusive lock requests on containers. |
| CONTAINER_SHARED_COUNT | BIGINT | Displays the number of shared lock requests on containers. |
| CONTAINER_COLLISION_COUNT | BIGINT | Displays the number of lock collisions on containers. |
| CONTAINER_TIMEOUT_COUNT | BIGINT | Displays the number of lock timeouts on containers. |
| SCHEMA_EXCLUSIVE_COUNT | BIGINT | Displays the number of exclusive lock requests on schemas. |
| SCHEMA_SHARED_COUNT | BIGINT | Displays the number of shared lock requests on schemas. |
| SCHEMA_COLLISION_COUNT | BIGINT | Displays the number of lock collisions on schemas. |
| SCHEMA_TIMEOUT_COUNT | BIGINT | Displays the number of lock timeouts on schemas. |
| OBJECT_EXCLUSIVE_COUNT | BIGINT | Displays the number of exclusive lock requests on objects |
| OBJECT_SHARED_COUNT | BIGINT | Displays the number of shared lock requests on objects. |
| OBJECT_COLLISION_COUNT | BIGINT | Displays the number of lock collisions on objects. |
| OBJECT_TIMEOUT_COUNT | BIGINT | Displays the number of timeouts on objects. |
| COMMITTED_REQUESTS_COUNT | BIGINT | Displays the number of committed requests. |

## Additional Information

This view is only usable if liveCache is enabled.

The liveCache uses its own lock-manager for object locks, container locks, and schema locks. This view shows the accumulated statistics of the lock requests to this lock-manager, which have been executed since restart.

This view has a resettable counterpart; you can see the values since the last reset in the M_LIVECACHE_LOCK_STATISTICS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_LIVECACHE_LOCK_STATISTICS_RESET;`.

## Related Information

M_LIVECACHE_LOCK_STATISTICS_RESET System View [→](M_LIVECACHE_LOCK_STATISTICS_RESET-System-View.md) M_LIVECACHE_LOCKS System View [→](M_LIVECACHE_LOCKS-System-View.md) LOCK TABLE Statement (Transaction Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/LOCK-TABLE-Statement-Transaction-Management.md)
