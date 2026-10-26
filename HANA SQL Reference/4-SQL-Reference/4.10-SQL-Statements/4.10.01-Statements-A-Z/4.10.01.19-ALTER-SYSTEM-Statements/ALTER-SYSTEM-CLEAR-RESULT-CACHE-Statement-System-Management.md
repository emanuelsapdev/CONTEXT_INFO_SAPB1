# 4.10.1.19.24 ALTER SYSTEM CLEAR RESULT CACHE Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 508–509

Removes all result cache entries from the system.

## Syntax

```sql
ALTER SYSTEM CLEAR [<cache_type>] RESULT CACHE
```

## Syntax Elements

#### cache_type

Setting `<cache_type>` to DYNAMIC ensures that the cache is refreshed every time a query on the result cache is run. The default value is STATIC.

```sql
<cache_type> ::= STATIC | DYNAMIC
```

## Description

The next suitable SELECT statement rebuilds the respective result cache entry.
