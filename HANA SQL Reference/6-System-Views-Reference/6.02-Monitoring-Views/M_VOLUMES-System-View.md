# 6.2.343 M_VOLUMES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2122–2123

Provides information about the volumes used by SAP HANA servers.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SERVICE_NAME | VARCHAR(32) | Displays the service name. |
| VOLUME_ID | INTEGER | Displays the volume ID. |
| SUBPATH | VARCHAR(512) | Displays the subpath appended to M_DISKS.PATH. |
| LIVECACHE_STORE | VARCHAR(10) | Displays whether the livecache is enabled. |
| REMOVE_STATUS | VARCHAR(16) | Displays the remove progress. |

## Related Information

M_VOLUME_SIZES System View [→](M_VOLUME_SIZES-System-View.md) M_VOLUME_FILES System View [→](M_VOLUME_FILES-System-View.md) M_DATA_VOLUME_STATISTICS System View [→](M_DATA_VOLUME_STATISTICS-System-View.md) M_PERSISTENT_MEMORY_VOLUME_STATISTICS System View [→](M_PERSISTENT_MEMORY_VOLUME_STATISTICS-System-View.md) M_PERSISTENT_MEMORY_VOLUMES System View [→](M_PERSISTENT_MEMORY_VOLUMES-System-View.md)
