# 6.1.75 FULL_SYSTEM_INFO_DUMPS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1495

Provides the FSIDs for the current database/tenant.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| FILE_NAME | NVARCHAR(512) | Displays the file name of the collection. |
| FILE_SIZE | BIGINT | Displays the file size in bytes. |
| FILE_MTIME | TIMESTAMP | Displays the date the file was modified. |
