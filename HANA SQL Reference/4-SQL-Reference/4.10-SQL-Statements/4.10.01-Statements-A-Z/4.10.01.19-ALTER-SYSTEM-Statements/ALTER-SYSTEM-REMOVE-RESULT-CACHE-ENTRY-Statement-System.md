# 4.10.1.19.47 ALTER SYSTEM REMOVE RESULT CACHE ENTRY Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 536–538

Removes the result cache entry for the specified cache ID.

## Syntax

```sql
ALTER SYSTEM REMOVE [<cache_type>] RESULT CACHE ENTRY <cache_id>;
```

## Syntax Elements

#### cache_type

Setting `<cache_type>` to DYNAMIC ensures that the cache is refreshed every time a query on the result cache is run. The default value is STATIC.

```sql
<cache_type> ::= STATIC | DYNAMIC
```

#### cache_id

Specifies the cache ID of the result cache entry according to the monitoring view. The M_RESULT_CACHE monitoring view provides cache IDs for static result caches and the M_DYNAMIC_RESULT_CACHE monitoring view provides cache IDs for dynamic result caches.

## Description

The next suitable SELECT statement rebuilds the respective result cache entry.

Removes the specified static result cache entry from the M_RESULT_CACHE view.

```sql
ALTER SYSTEM REMOVE STATIC RESULT CACHE ENTRY <cache-ID>;
```

Removes the specified dynamic result cache entry from the M_DYNAMIC_RESULT_CACHE view.

```sql
ALTER SYSTEM REMOVE DYNAMIC RESULT CACHE ENTRY <cache-ID>;
```

## Related Information

ALTER SYSTEM REFRESH RESULT CACHE ENTRY Statement (System Management) [→](ALTER-SYSTEM-REFRESH-RESULT-CACHE-ENTRY-Statement-System.md) M_RESULT_CACHE System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_RESULT_CACHE-System-View.md) M_DYNAMIC_RESULT_CACHE System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_DYNAMIC_RESULT_CACHE-System-View.md)
