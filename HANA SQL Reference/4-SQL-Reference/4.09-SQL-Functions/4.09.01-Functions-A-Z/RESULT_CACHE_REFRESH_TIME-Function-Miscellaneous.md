# 4.9.1.159 RESULT_CACHE_REFRESH_TIME Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 295–296

Returns the last cache refresh time of a result cache entry.

## Syntax

```sql
RESULT_CACHE_REFRESH_TIME()
```

## Description

If no result cache entry is provided, then NULL is returned.

## Example

The following fictitious example returns the last cache refresh time of the result cache entry V1, `2015-11-20 01:01:01.010101`.

```sql
SELECT DISTINCT RESULT_CACHE_REFRESH_TIME() FROM V1;
```
