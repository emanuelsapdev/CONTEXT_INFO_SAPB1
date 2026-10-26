# 4.10.1.19.46 ALTER SYSTEM REFRESH RESULT CACHE ENTRY Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 535–536

Refreshes the specified result cache entry.

## Syntax

```sql
ALTER SYSTEM REFRESH [<cache_type>] RESULT CACHE ENTRY <cache_id>;
```

## Syntax Elements

#### cache_type

Specifies the cache type. The default value is STATIC.

```sql
<cache_type> ::= STATIC
```

#### cache_id

Specifies the cache ID of the result cache entry according to the monitoring view. The M_RESULT_CACHE monitoring view provides cache IDs for static result caches.

## Description

Refreshes the result cache entry specified by the `<cache_id>`. No subsequent SELECT statement is required.

## Examples

Refresh the specified static result cache entry from the M_RESULT_CACHE view.

```sql
ALTER SYSTEM REFRESH STATIC RESULT CACHE ENTRY <cache-ID>;
```

## Related Information

[M_RESULT_CACHE System View](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_RESULT_CACHE-System-View.md)
