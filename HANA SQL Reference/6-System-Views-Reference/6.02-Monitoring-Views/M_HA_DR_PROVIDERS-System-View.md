# 6.2.121 M_HA_DR_PROVIDERS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1809

Provides information about loaded HA/DR providers.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| PROVIDER_NAME | VARCHAR(64) | Displays the HA/DR provider name. |
| PROVIDER_COMPANY | VARCHAR(64) | Displays the HA/DR provider company name. |
| PROVIDER_DESCRIPTION | VARCHAR(2000) | Displays the HA/DR provider description. |
| PROVIDER_VERSION | VARCHAR(32) | Displays theHA/DR provider version. |
| PROVIDER_TYPE | VARCHAR(32) | Displays the HA/DR provider type. |
| PROVIDER_PATH | VARCHAR(512) | Displays the HA/DR provider path. |
| EXECUTION_ORDER | INTEGER | Displays the HA/DR provider execution order. |
