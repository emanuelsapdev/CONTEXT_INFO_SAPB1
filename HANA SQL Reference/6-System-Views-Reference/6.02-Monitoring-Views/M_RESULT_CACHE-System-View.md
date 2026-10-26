# 6.2.237 M_RESULT_CACHE System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1965–1967

Provides result cache information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| CACHE_ID | BIGINT | Displays the unique ID for each result cache entry. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| OBJECT_NAME | NVARCHAR(256) | Displays the object name. |
| OBJECT_TYPE | VARCHAR(32) | Displays the object type. |
| USER_NAME | NVARCHAR(256) | Displays the user name. |
| DETAILS | NCLOB | Displays the details. |
| MEMORY_SIZE | BIGINT | Displays the size of memory occupied by the result cache entry in bytes. |
| RECORD_COUNT | BIGINT | Displays the number of records in the cache entry. |
| CREATE_TIME | TIMESTAMP | Displays the timestamp the result cache entry is generated and stored. |
| LAST_REFRESH_TIME | TIMESTAMP | Displays the last refresh time of the result cache entry. |
| LAST_REFRESH_DURATION | BIGINT | Displays the time duration of the cache entry preparation in milliseconds. |
| REFRESH_COUNT | BIGINT | Displays the number of refreshments on the cache entry. |
| LAST_ACCESS_TIME | TIMESTAMP | Displays the last time the result cache entry was accessed by a user. |
| ACCESS_COUNT | BIGINT | Displays the number of accesses on the cache entry. |
| RUNTIME_MISS_COUNT | BIGINT | Displays the number of cache miss counts. This value is decided at runtime with parameter values. |
| EVICT_COUNT | BIGINT | Displays the total number of eviction counts due to budget limitations. |
| IS_EVICTED | VARCHAR(5) | Displays whether or not the cache entry is evicted: TRUE/FALSE. |
