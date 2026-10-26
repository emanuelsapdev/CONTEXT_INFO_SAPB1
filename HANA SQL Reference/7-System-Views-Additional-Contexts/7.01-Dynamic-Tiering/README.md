# 7.1 Dynamic Tiering

> [↑ 7 System Views Reference for Additional SAP HANA Contexts](../README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2161–2162

> **Caution**
>
> This guide contains syntax variations for different product contexts. These are handled as separate reference topics that have titles that announce the context in square brackets at the end of the title. The guide is also organized to keep reference topics together for a context. Always be sure you are using the SQL reference topic specific to your context.

M_ES_CONNECTIONS System View [Dynamic Tiering] [→](7.01.01-M_ES_CONNECTIONS-System-View-Dynamic-Tiering.md)

Processes running in SAP HANA dynamic tiering.

M_ES_DBSPACE_FILES System View [Dynamic Tiering] [→](7.01.02-M_ES_DBSPACE_FILES-System-View-Dynamic-Tiering.md)

Shows information of all dbspace files in the extended storage.

M_ES_DBSPACES System View [Dynamic Tiering] [→](7.01.03-M_ES_DBSPACES-System-View-Dynamic-Tiering.md)

Shows the dbspace configured in extended storage.

M_ES_DELTA_MEMORY System View [Dynamic Tiering] [→](7.01.04-M_ES_DELTA_MEMORY-System-View-Dynamic-Tiering.md)

Delta memory utilization inSAP HANA dynamic tiering.

M_ES_DELTA_MERGE_STATISTICS System View [Dynamic Tiering] [→](7.01.05-M_ES_DELTA_MERGE_STATISTICS-System-View-Dynamic-Tiering.md)

History of internal and user driven merge operations for delta enabled extended tables.

M_ES_EXPENSIVE_STATEMENTS System View [Dynamic Tiering] [→](7.01.06-M_ES_EXPENSIVE_STATEMENTS-System-View-Dynamic-Tiering.md)

Provides an interface to give system administrators more visibility into where time and resources are being spent during statement executions that involve extended storage. The information is a result of the union of M_EXPENSIVE_STATEMENTS and M_REMOTE_STATEMENTS.

M_ES_LOCKS System View [Dynamic Tiering] [→](7.01.07-M_ES_LOCKS-System-View-Dynamic-Tiering.md)

Locks held in SAP HANA dynamic tiering.

M_ES_OVERVIEW System View [Dynamic Tiering] [→](7.01.08-M_ES_OVERVIEW-System-View-Dynamic-Tiering.md)

Status information of SAP HANA dynamic tiering as named value pair.

M_ES_RESULT_CACHE [Dynamic Tiering] [→](7.01.09-M_ES_RESULT_CACHE-Dynamic-Tiering.md)

Status information on the result cache storage for SAP HANA dynamic tiering.

M_ES_TABLES System View [Dynamic Tiering] [→](7.01.10-M_ES_TABLES-System-View-Dynamic-Tiering.md)

Shows information for all extended tables in extended storage.

M_ES_TRANSACTIONS System View [Dynamic Tiering] [→](7.01.11-M_ES_TRANSACTIONS-System-View-Dynamic-Tiering.md)

Active transactions in SAP HANA dynamic tiering.

Additional System Views [Dynamic Tiering] [→](7.01.12-Additional-System-Views-Dynamic-Tiering.md)

Views including information pertaining to, but not limited to, SAP HANA dynamic tiering.

## Contenido de esta sección

- [7.1.1 M_ES_CONNECTIONS System View [Dynamic Tiering]](7.01.01-M_ES_CONNECTIONS-System-View-Dynamic-Tiering.md)
- [7.1.2 M_ES_DBSPACE_FILES System View [Dynamic Tiering]](7.01.02-M_ES_DBSPACE_FILES-System-View-Dynamic-Tiering.md)
- [7.1.3 M_ES_DBSPACES System View [Dynamic Tiering]](7.01.03-M_ES_DBSPACES-System-View-Dynamic-Tiering.md)
- [7.1.4 M_ES_DELTA_MEMORY System View [Dynamic Tiering]](7.01.04-M_ES_DELTA_MEMORY-System-View-Dynamic-Tiering.md)
- [7.1.5 M_ES_DELTA_MERGE_STATISTICS System View [Dynamic Tiering]](7.01.05-M_ES_DELTA_MERGE_STATISTICS-System-View-Dynamic-Tiering.md)
- [7.1.6 M_ES_EXPENSIVE_STATEMENTS System View [Dynamic Tiering]](7.01.06-M_ES_EXPENSIVE_STATEMENTS-System-View-Dynamic-Tiering.md)
- [7.1.7 M_ES_LOCKS System View [Dynamic Tiering]](7.01.07-M_ES_LOCKS-System-View-Dynamic-Tiering.md)
- [7.1.8 M_ES_OVERVIEW System View [Dynamic Tiering]](7.01.08-M_ES_OVERVIEW-System-View-Dynamic-Tiering.md)
- [7.1.9 M_ES_RESULT_CACHE [Dynamic Tiering]](7.01.09-M_ES_RESULT_CACHE-Dynamic-Tiering.md)
- [7.1.10 M_ES_TABLES System View [Dynamic Tiering]](7.01.10-M_ES_TABLES-System-View-Dynamic-Tiering.md)
- [7.1.11 M_ES_TRANSACTIONS System View [Dynamic Tiering]](7.01.11-M_ES_TRANSACTIONS-System-View-Dynamic-Tiering.md)
- [7.1.12 Additional System Views [Dynamic Tiering]](7.01.12-Additional-System-Views-Dynamic-Tiering.md)
