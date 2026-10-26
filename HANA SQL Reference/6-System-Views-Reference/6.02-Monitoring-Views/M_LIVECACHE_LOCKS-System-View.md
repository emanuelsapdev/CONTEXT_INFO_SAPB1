# 6.2.152 M_LIVECACHE_LOCKS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1855–1856

Detailed information on the Object Management System (OMS) locks.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| ID | VARCHAR(20) | Displays the ID of the lock: OID, container ID, or schema ID, depending on the lock class. |
| CONTAINER_ID | BIGINT | Displays the ID of the corresponding container. |
| CLASS | VARCHAR(20) | Displays the class that the lock belongs to. |
| GRANTED_MODE | VARCHAR(20) | Displays the mode that the lock has granted to some request(s). |
| MODE | VARCHAR(20) | Displays the mode that the request is requesting on the lock: Free, Intend Share, IntendExclusive, Share, ShareIn tendExclusive, or Exclusive. |
| TYPE | VARCHAR(10) | Displays when the lock can be removed, either at transaction-end (EOT) or if not visible anymore (Consistent). |
| STATE | VARCHAR(10) | Displays the state of the lock request. |
| TID | BIGINT | Displays the transaction ID belonging to this lock request. |
| TIMEOUT | BIGINT | Displays remaining timeout, if a timeout is specified. |

## Additional Information

The liveCache uses its own lock-manager for object locks, container locks, and schema locks. This view shows information about all the locks, which are currently kept in this lock manager.

Exclusive locks on objects are in most cases not managed by this lock manager, but the necessary lock-information is stored in the respective object header.

This view can only be used if liveCache is enabled.

## Related Information

M_LIVECACHE_LOCK_STATISTICS_RESET System View [→](M_LIVECACHE_LOCK_STATISTICS_RESET-System-View.md) M_LIVECACHE_LOCK_STATISTICS System View [→](M_LIVECACHE_LOCK_STATISTICS-System-View.md) LOCK TABLE Statement (Transaction Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/LOCK-TABLE-Statement-Transaction-Management.md)
