# 6.1.68 ENCRYPTION_ROOT_KEYS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1480–1481

Provides information about root keys.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| ROOT_KEY_TYPE | VARCHAR(16) | Displays the usage type of the root key: PERSISTENCE, DPAPI, LOG, BACKUP. |
| ROOT_KEY_VERSION | INTEGER | Deprecated: The version of the root key. |
| CREATE_TIMESTAMP | TIMESTAMP | Displays the creation time of the root key (UTC). |
| IS_CONSISTENT | VARCHAR(5) | Displays whether the key is consistent between persistence and the SSFS file: TRUE/FALSE. |
| RESET_COUNT | INTEGER | Displays the number of consistency re sets. |
| IS_USED | VARCHAR(5) | Displays whether key version is the version used for encryption: TRUE/FALSE. |
| ROOT_KEY_STATUS | VARCHAR(11) | Displays the state of the root key: AC TIVE, PREACTIVE, or DEACTIVATED. |
| ROOT_KEY_HASH | VARCHAR(64) | Displays the root key hash value. |
| IN_BACKUP | VARCHAR(5) | Displays whether root key has been previously backed up: TRUE/FALSE. |

## Related Information

[ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS Function (Security)](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS-Function-Security.md)

ENCRYPTION_ROOT_KEYS_HAS_BACKUP_PASSWORD Function (Security) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ENCRYPTION_ROOT_KEYS_HAS_BACKUP_PASSWORD-Function-Security.md) ALTER SYSTEM SET ENCRYPTION ROOT KEYS BACKUP PASSWORD Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-SET-ENCRYPTION-ROOT-KEYS-BACKUP-PASSWORD.md) ALTER SYSTEM VALIDATE ENCRYPTION ROOT KEYS BACKUP PASSWORD Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-VALIDATE-ENCRYPTION-ROOT-KEYS-BACKUP-PASSWORD.md) ALTER SYSTEM PERSISTENCE ENCRYPTION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-PERSISTENCE-ENCRYPTION-Statement-System.md) ALTER SYSTEM BACKUP ENCRYPTION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-BACKUP-ENCRYPTION-Statement-System-Management.md) ALTER SYSTEM LOG ENCRYPTION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-LOG-ENCRYPTION-Statement-System-Management.md) ALTER SYSTEM APPLICATION ENCRYPTION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-APPLICATION-ENCRYPTION-Statement-System.md) M_ENCRYPTION_OVERVIEW System View [→](../6.02-Monitoring-Views/M_ENCRYPTION_OVERVIEW-System-View.md) M_PERSISTENCE_ENCRYPTION_STATUS System View [→](../6.02-Monitoring-Views/M_PERSISTENCE_ENCRYPTION_STATUS-System-View.md) Client-side Encryption Statements [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.07-Client-side-Encryption-Statements.md)
