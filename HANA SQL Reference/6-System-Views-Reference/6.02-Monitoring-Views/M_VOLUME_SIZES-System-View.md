# 6.2.355 M_VOLUME_SIZES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 2148

Provides information about volume sizes used by SAP HANA servers.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| VOLUME_ID | INTEGER | Displays the volume ID. See M_VOLUMES. |
| DISK_ID | INTEGER | Displays the disk ID. See M_DISKS. |
| DATA_SIZE | BIGINT | Displays the data area size in bytes. |
| LOG_SIZE | BIGINT | Displays the log area size in bytes. |

## Related Information

M_DISKS System View [→](M_DISKS-System-View.md) M_VOLUMES System View [→](M_VOLUMES-System-View.md)
