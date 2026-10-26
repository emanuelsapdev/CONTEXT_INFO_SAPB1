# 6.2.247 M_SECURESTORE System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1982–1983

Provides secure store monitoring information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| KEY_TYPE | VARCHAR(12) | Displays the type of encryption key. |
| IS_CONSISTENT | VARCHAR(5) | Indicates whether or not the key is consistent between the persistence and the SSFS file: TRUE/FALSE. |
| RESET_COUNT | INTEGER | Displays the number of consistency re sets. |
| VERSION | INTEGER | Displays the version of the key. |
| IS_CURRENT | VARCHAR(5) | Indicates whether or not the key version is the current version in the SSFS file: TRUE/FALSE. |
