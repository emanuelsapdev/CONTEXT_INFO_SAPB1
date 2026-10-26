# 6.2.201 M_PERSISTENCE_ENCRYPTION_STATUS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1926–1927

Provides information about persistence encryption.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| ENCRYPTION_ACTIVE | VARCHAR(5) | Displays whether or not the encryption is currently active for writing into persistence: TRUE/FALSE. |
| ENCRYPTION_ACTIVE_AFTER_NEXT_SAVEPOINT | VARCHAR(5) | Displays whether or not the encryption is active for writing into persistence after the next savepoint: TRUE/FALSE. |
| KEY_CHANGE_WITH_NEXT_SAVEPOINT | VARCHAR(5) | Displays whether or not the next save point activates a new key: TRUE/ FALSE. |
| ROOT_KEY_CHANGE_WITH_NEXT_SAVEPOINT | VARCHAR(5) | Displays whether or not the next save point activates a new root key: TRUE/ FALSE. |
| IS_LATEST_ROOT_KEY_VERSION | VARCHAR(5) | Displays whether or not the used root key version is the newest one: TRUE/ FALSE. |
| USED_ROOT_KEY_VERSION | INTEGER | Deprecated. |
| DATA_CONVERSION_ACTIVE | VARCHAR(5) | Displays whether or not the conversion of data to the latest encryption status or key is active: TRUE/FALSE. |
| KEY_PAGE_ENTRY_COUNT | BIGINT | Displays the number of entries within the key page. |
| USED_ROOT_KEY_HASH | VARCHAR(64) | Displays the hash of the root key that this service is using. |

## Related Information

M_PERSISTENCE_ENCRYPTION_KEYS System View [→](M_PERSISTENCE_ENCRYPTION_KEYS-System-View.md) ALTER SYSTEM PERSISTENCE ENCRYPTION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-PERSISTENCE-ENCRYPTION-Statement-System.md)
