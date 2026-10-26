# 6.2.14 M_ATTACHED_STORAGES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1652–1653

Provides information about currently attached devices.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host. |
| STORAGE_ID | INTEGER | Displays the storage ID. |
| PATH | VARCHAR(512) | Displays the path for the currently attached devices. |
| KEY | VARCHAR(256) | Displays the key for the currently attached devices. This information is provided by the creator of a specific storage connector. |
| VALUE | VARCHAR(2000) | Displays additional information about currently attached devices provided by the creator of a specific storage connector. |
