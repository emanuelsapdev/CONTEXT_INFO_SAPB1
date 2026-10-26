# 6.2.49 M_CONTAINER_DIRECTORY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1698–1700

Provides container directory statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| CNT_CREATE | BIGINT | Displays the number of creates. |
| CNT_CREATE_ROLLBACK | BIGINT | Displays the number of rolled back creates. |
| CNT_REMOVE | BIGINT | Displays the number of removes. |
| CNT_REMOVE_FAIL | BIGINT | Displays the number of failed removes. |
| CNT_REMOVE_ROLLBACK | BIGINT | Displays the number of rolled back re moves. |
| CNT_MOVE | BIGINT | Displays the number of moves. |
| CNT_GET_PHYSICALSIZE | BIGINT | Displays the number of getPhysicalSize. |
| CNT_GET | BIGINT | Displays the number of retrieved containers. |
| CNT_GET_FAIL | BIGINT | Displays the number of failed gets. |
| CNT_BEGIN | BIGINT | Displays the number of used iterators. |
| CNT_ITERATED | BIGINT | Displays the number of iterated containers. |
| CNT_CACHEHIT | BIGINT | Displays the number of cache hits. |
| CNT_CACHEMISS | BIGINT | Displays the number of cache misses. |
| CNT_CONTAINERS | BIGINT | Displays the number of existing containers. |

## Related Information

M_CONTAINER_NAME_DIRECTORY System View [→](M_CONTAINER_NAME_DIRECTORY-System-View.md) CONTAINS Predicate [→](../../4-SQL-Reference/4.07-Predicates/4.07.03-CONTAINS-Predicate.md)
