# 6.2.38 M_CLIENT_VERSIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1678

Provides versions of all supported client applications.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| CLIENT_TYPE | VARCHAR(256) | Displays the type of client, for example, ABAP_FDA or BI Modeler. |
| CLIENT_RELEASE_ID | SMALLINT | Displays the technical release ID. |
| CLIENT_RELEASE_DESC | VARCHAR(256) | Displays the human readable release description. |
| MIN_VERSION | SMALLINT | Displays the lowest supported protocol version. |
| MAX_VERSION | SMALLINT | Displays the highest supported protocol version. |
