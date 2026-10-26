# 6.2.200 M_PERSISTENCE_ENCRYPTION_KEYS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1925–1926

Provides information about encryption page keys.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VALID_FROM_SAVEPOINT | INTEGER | Displays the valid from savepoint version. |
| VALID_FROM_TIMESTAMP | TIMESTAMP | Displays the valid from timestamp, in microseconds, given in UTC. |
| IS_ENCRYPTED | VARCHAR(5) | Indicates whether or not the persistence encryption is active: TRUE/ FALSE. |

## Related Information

M_PERSISTENCE_ENCRYPTION_STATUS System View [→](M_PERSISTENCE_ENCRYPTION_STATUS-System-View.md) ALTER SYSTEM PERSISTENCE ENCRYPTION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-PERSISTENCE-ENCRYPTION-Statement-System.md)
