# 6.2.50 M_CONTAINER_NAME_DIRECTORY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1700–1701

Provides ContainerNameDirectory statistics.

## Structure

| **Column name** | **Data type** | **Unit** | **Description** |
| --- | --- | --- | --- |
| HOST | VARCHAR(64) |   | Displays the host name. |
| PORT | INTEGER |   | Displays the internal port. |
| VOLUME_ID | INTEGER |   | Displays the persistence volume ID. |
| CNT_CREATE | BIGINT | Counter | Displays the create counts. |
| CNT_CREATE_FAIL | BIGINT | Counter | Displays the number of failed creates. |
| CNT_INITIAL_CREATE | BIGINT | Counter | Displays the number of creates on the load. |
| CNT_INITIAL_SKIP | BIGINT | Counter | Displays the number of skips on the load. |
| CNT_REMOVE | BIGINT | Counter | Displays the number of re moves. |
| CNT_REMOVE_FAIL | BIGINT | Counter | Displays the number of failed removes. |
| CNT_REMOVE_ALL | BIGINT | Counter | Displays the number of re moveAll. |
| CNT_RENAME | BIGINT | Counter | Displays the number of re names. |
| CNT_RENAME_FAIL | BIGINT | Counter | Displays the number of failed renames. |
| CNT_EXISTS | BIGINT | Counter | Displays the number of checked containers. |
| CNT_GET | BIGINT | Counter | Displays the number of retrieved containers. |
| CNT_GET_FAIL | BIGINT | Counter | Displays the number of failed gets. |
| CNT_BEGIN | BIGINT | Counter | Displays the number of used iterators. |
| CNT_ITERATE | BIGINT | Counter | Displays the number of iterated containers. |
| CNT_CONTAINERS | BIGINT | Counter | Displays the number of existing containers. |

## Related Information

M_CONTAINER_DIRECTORY System View [→](M_CONTAINER_DIRECTORY-System-View.md) CONTAINS Predicate [→](../../4-SQL-Reference/4.07-Predicates/4.07.03-CONTAINS-Predicate.md)
