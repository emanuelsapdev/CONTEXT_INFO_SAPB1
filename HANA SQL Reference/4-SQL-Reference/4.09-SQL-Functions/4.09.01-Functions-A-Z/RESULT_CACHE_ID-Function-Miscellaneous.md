# 4.9.1.158 RESULT_CACHE_ID Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 294–295

Returns the cache ID of a result cache entry.

## Syntax

```sql
RESULT_CACHE_ID()
```

## Description

If no result cache entry is specified, then NULL is returned.

## Example

The following fictitious example returns the cache ID for result cache entry V1, `40000001`.

```sql
SELECT DISTINCT RESULT_CACHE_ID () FROM V1 WITH HINT(RESULT_CACHE);
```
