# 6.2.98 M_ES_DBSPACE_FILES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1774–1775

Provides extended storage dbspace file information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the volume ID. |
| DBSPACE_NAME | VARCHAR(128) | Displays the name of the dbspace. |
| DBSPACE_FILE_NAME | VARCHAR(128) | Displays the name of the dbspace file. |
| STATUS | VARCHAR(7) | Displays the status of the dbspace: OFFLINE/ONLINE. |
| MODE | VARCHAR(9) | Displays the dbspace mode: RE ADONLY/READWRITE. |
| USAGE | DOUBLE | Displays the percent of dbspace in use. |
| PATH | VARCHAR(512) | Displays the physical path of the file. |
| TOTAL_SIZE | BIGINT | Displays the total size of the dbspace in bytes. |
| RESERVED_SIZE | BIGINT | Displays the total reserved space, in bytes, that can be added to dbfiles in the dbspace. |
| DISK_STRIPE_SIZE | BIGINT | Displays the disk stripe size in bytes. |
| IS_DROP_ALLOWED | VARCHAR(5) | Displays whether or not the dbspace can be dropped: TRUE/FALSE. |

## Related Information

M_ES_DBSPACES System View [→](M_ES_DBSPACES-System-View.md) ALTER EXTENDED STORAGE Statement [Dynamic Tiering] [→](../../5-Additional-SAP-HANA-Contexts/5.02-Dynamic-Tiering/ALTER-EXTENDED-STORAGE-Statement-Dynamic-Tiering.md)
