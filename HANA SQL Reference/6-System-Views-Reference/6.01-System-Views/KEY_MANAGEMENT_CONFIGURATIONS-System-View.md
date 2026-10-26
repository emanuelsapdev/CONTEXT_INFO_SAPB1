# 6.1.93 KEY_MANAGEMENT_CONFIGURATIONS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1511–1512

Displays information about the existing key management configurations.

## Structure

| **Column** | **Data Type** | **Description** |
| --- | --- | --- |
| DATABASE_NAME | NVARCHAR(256) | Displays the database name. |
| CONFIGURATION_NAME | NVARCHAR(256) | Displays the name of the key management configuration. |
| IS_ACTIVE | NVARCHAR(5) | Indicates whether this configuration is used by LSS to define access to SAP HANA's sensitive information. |
| TYPE | NVARCHAR(20) | Displays the type of external key management. |
| CLIENT_VERSION | NVARCHAR(12) | Displays the version of the driver software. |
| PROPERTIES | NCLOB | Displays a reduced version of the properties section of the `<settings>` JSON (the "credentials" object is omitted). |
