# 6.2.86 M_DISKS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1759–1760

Provides information about disk configuration and utilization of the host machine.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| DISK_ID | INTEGER | Displays the disk ID. |
| DEVICE_ID | BIGINT | Displays the database internal device ID. |
| HOST | VARCHAR(64) | Displays the host name. This is only set if the disk is used by exactly one host. |
| PATH | VARCHAR(512) | Displays the path. |
| SUBPATH | VARCHAR(512) | Displays the subpath. |
| FILESYSTEM_TYPE | VARCHAR(32) | Displays the filesystem type. |
| USAGE_TYPE | VARCHAR(64) | Displays the usage type. Values are: LOG, DATA, TRACE, DATA_BACKUP, LOG_BACKUP, CATALOG_BACKUP, or XSA_WORKSPACE. |
| TOTAL_SIZE | BIGINT | Displays the volume of the used space in bytes. |
| USED_SIZE | BIGINT | Displays the volume size in bytes. |
| TOTAL_DEVICE_SIZE | BIGINT | Displays the total device size returned by the operating system in bytes. |
| MOUNT_SOURCE | VARCHAR(512) | Displays the source of the mount. |
| MOUNT_PATH | VARCHAR(512) | Displays the mount path. |
| MOUNT_DETAILS | VARCHAR(2000) | Displays the mount details as stated in `/proc/mount`. |

## Related Information

[M_DISK_USAGE System View](M_DISK_USAGE-System-View.md)
