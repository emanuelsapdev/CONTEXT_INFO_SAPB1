# 6.2.360 M_XS_APPLICATIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2157–2158

Provides information about applications deployed and running in SAP HANA XS.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| APPLICATION_NAME | NVARCHAR(256) | Displays the name of the application. |
| DELIVERY_UNIT | NVARCHAR(256) | Displays the name of the delivery unit that this application belongs to. |
| VENDOR | NVARCHAR(256) | Displays the vendor of the delivery unit. |
| VERSION | NVARCHAR(256) | Displays the version information of the delivery unit. |
| VERSION_SP | NVARCHAR(16) | Displays the SP version information of the delivery unit. |
| VERSION_PATCH | NVARCHAR(16) | Displays the patch version information of the delivery unit. |

## Related Information

M_XS_APPLICATION_ISSUES System View [→](M_XS_APPLICATION_ISSUES-System-View.md) M_XS_PUBLIC_URLS System View [→](M_XS_PUBLIC_URLS-System-View.md) M_XS_SESSIONS System View [→](M_XS_SESSIONS-System-View.md) ALL_AUDIT_LOG System View [→](../6.01-System-Views/ALL_AUDIT_LOG-System-View.md) AUDIT_LOG System View [→](../6.01-System-Views/AUDIT_LOG-System-View.md)
