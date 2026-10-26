# 6.2.73 M_DATABASE_HISTORY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1739

Provides installation version history.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| INSTALL_TIME | TIMESTAMP | Displays the installation or first start time. |
| VERSION | VARCHAR(32) | Displays the version: major.mi nor.patch.build. |

## Related Information

M_DATABASE System View [→](M_DATABASE-System-View.md) M_DATABASES System View [→](M_DATABASES-System-View.md) PERSISTENCE_HISTORY System View [→](../6.01-System-Views/PERSISTENCE_HISTORY-System-View.md) M_DATABASE_REPLICAS System View [→](M_DATABASE_REPLICAS-System-View.md) M_DATABASE_REPLICA_STATISTICS System View [→](M_DATABASE_REPLICA_STATISTICS-System-View.md)
