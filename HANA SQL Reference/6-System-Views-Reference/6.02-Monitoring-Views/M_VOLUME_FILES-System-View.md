# 6.2.344 M_VOLUME_FILES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2123–2124

Provides information about volume files.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| FILE_TYPE | VARCHAR(16) | Displays the type of file: DATA, LOG, and so on. |
| FILE_NAME | VARCHAR(256) | Displays the file name. |
| USED_SIZE | BIGINT | Displays the size of used data within the file in bytes. |
| TOTAL_SIZE | BIGINT | Displays the total file size in bytes. |

## Additional Information

Displays information about files in the volume directories. All files in these directories are shown, but only registered files (files currently used by the database) have a file type. `TOTAL_SIZE` is the size as reported by the file system.

The meaning of `USED_SIZE` depends on the file type:

- **DATA:** Displays the size of used and shadow pages in the data volume file.
- **LOG:** Displays that the used size equals the `TOTAL_SIZE`.

## Related Information

M_DATA_VOLUME_PARTITION_STATISTICS System View [→](M_DATA_VOLUME_PARTITION_STATISTICS-System-View.md) M_DATA_VOLUME_STATISTICS System View [→](M_DATA_VOLUME_STATISTICS-System-View.md)
