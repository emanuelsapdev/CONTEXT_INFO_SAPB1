# 6.2.87 M_DISK_USAGE System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1760–1761

Provides disk usage information on host basis group by resource types.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| USAGE_TYPE | VARCHAR(11) | Displays the resource type: LOG, DATA, TRACE, LOG_BACKUP or DATA_BACKUP. |
| USED_SIZE | BIGINT | Displays the size of the used disk space in bytes. |

## Related Information

[M_DISKS System View](M_DISKS-System-View.md)
