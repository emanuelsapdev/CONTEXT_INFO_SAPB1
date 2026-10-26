# 4.10.1.19.21 ALTER SYSTEM CLEAR CACHE Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 505–506

Clears resources (entries) from one or more cache instances.

## Syntax

```sql
ALTER SYSTEM CLEAR CACHE ( <cache_id> [, <cache_id> […] ] [ SYNC ] )
```

## Syntax Elements

#### cache_id

Specifies the ID of the cache instance to clear, as found in the M_CACHES system view.

#### SYNC

Increases the retry attempts for resources (entries) that were initially blocked from clearing. Specifying SYNC may make this statement take longer to return (for example if many retries were required) but performs a better clearing operation than without specifying SYNC.

## Description

Executing this statement clears the specified cache instances not only on the local (index) server, but across all distributed instances of the cache.

Entries (resources) in a cache instance may be blocked from clearing. This can happen while entries are being inserted or searched for, or when entries are being fetched for display in M_CACHE_ENTRIES. There may be other reasons why entries are blocked from clearing as well, so after a clearing operation (even if SYNC is specified), some entries may still remain in the cache instance.

When SYNC is not specified, the HANA server makes a best attempt effort at clearing as many cache entries as possible, and the statement always succeeds.

When SYNC is specified, the HANA server increases the number of retry attempts on resources that were initially busy. If there are distributed instances of the cache, then the command is successful only if each local clearing operation succeeds without exceeding the timeout for cache distributed requests (ini parameter [cache] resultcache_request_timeout_in_milliseconds). With SYNC, the statement may return a general error (error number 2) if the clear operation failed to clear some entries.

Regardless of whether SYNC is specified, the M_CACHE_ENTRIES system view may still return entries immediately after the ALTER SYSTEM CLEAR CACHE statement is run. This can happen if the clearing operation occurred concurrently with other database operations.

## Related Information

[M_CACHE_ENTRIES System View](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_CACHE_ENTRIES-System-View.md)
