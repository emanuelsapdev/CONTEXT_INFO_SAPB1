# 6.2.211 M_PLUGIN_STATUS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1937–1938

Provides status for plugins.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| PLUGIN_NAME | VARCHAR(32) | Displays the subdirectory, containing executables and plugins, where the files of an AFL area are located. There can be several areas per subdirectory. |
| ERROR_TEXT | NVARCHAR(1024) | Displays the error message in case a package or AFL cannot be registered. |
| AREA_NAME | NVARCHAR(256) | Displays the name of an area. |
| AREA_STATUS | VARCHAR(32) | Displays the status of an area: REGIS TRATION SUCCESSFUL, REGISTRA TION FAILED, or REGISTRATION SKIP PED. |
| PACKAGE_NAME | NVARCHAR(256) | Displays the name of a package, which is an internal representation of an AFL. There can be several packages per area. |
| PACKAGE_STATUS | VARCHAR(32) | Displays the status of a package: REG ISTRATION SUCCESSFUL, REGISTRA TION FAILED, or REGISTRATION SKIP PED. |

## Related Information

[M_PLUGIN_MANIFESTS System View](M_PLUGIN_MANIFESTS-System-View.md)
