# 6.2.362 M_XS_PUBLIC_URLS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 2159

Provides a list of URLs under which this database can be reached.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HTTP_URL | VARCHAR(270) | Displays the public HTTP URL of the XS Engine. |
| HTTPS_URL | VARCHAR(270) | Displays the public HTTPS URL of the XS Engine. |
| PURPOSE | VARCHAR(32) | Displays the purpose of these URLs. |

## Related Information

M_XS_SESSIONS System View [→](M_XS_SESSIONS-System-View.md) M_XS_APPLICATIONS System View [→](M_XS_APPLICATIONS-System-View.md) M_XS_APPLICATION_ISSUES System View [→](M_XS_APPLICATION_ISSUES-System-View.md)
