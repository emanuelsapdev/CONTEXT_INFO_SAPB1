# 6.1.20 APPLICATION_ENCRYPTION_KEYS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1421–1422

Provides information about encryption keys used by applications.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| COMPONENT | NVARCHAR(20) | Displays the component that the key belongs to. |
| SUB_COMPONENT | NVARCHAR(512) | Displays the subcomponent that the key belongs to. |
| CREATOR | NVARCHAR(256) | Displays the database user or the internal subcomponent that created the key. |
| CREATE_TIMESTAMP | TIMESTAMP | Displays the timestamp when the key was created. |
| IS_CURRENT | VARCHAR(5) | Displays whether the key is used by the subcomponent for newly encrypted data: TRUE/FALSE. |

## Related Information

M_ENCRYPTION_OVERVIEW System View [→](../6.02-Monitoring-Views/M_ENCRYPTION_OVERVIEW-System-View.md) ALTER SYSTEM APPLICATION ENCRYPTION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-APPLICATION-ENCRYPTION-Statement-System.md) ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS Function (Security) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS-Function-Security.md) ENCRYPTION_ROOT_KEYS_HAS_BACKUP_PASSWORD Function (Security) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/ENCRYPTION_ROOT_KEYS_HAS_BACKUP_PASSWORD-Function-Security.md)
