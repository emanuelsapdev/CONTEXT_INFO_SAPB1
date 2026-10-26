# 4.10.1.19.53 ALTER SYSTEM SET ENCRYPTION ROOT KEYS BACKUP PASSWORD Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 543–545

Sets a password for encrypting root key backups.

## Syntax

```sql
ALTER SYSTEM SET ENCRYPTION ROOT KEYS BACKUP PASSWORD <password>
```

## Syntax Elements

#### password

The specified password overwrites any existing password.

## Description

This statement must be executed in the database for which the root key backup password is being specified.

The password is stored in the encryption root key store (instance SSFS or local secure store (LSS)).

For more information about encryption in the SAP HANA database, see the SAP HANA Security Guide and the SAP HANA Administration Guide.

## Permissions

You must have the ENCRYPTION ROOT KEY ADMIN privilege to execute this statement.

## Example

Set a password that is used to protect root key backups.

```sql
ALTER SYSTEM SET ENCRYPTION ROOT KEYS BACKUP PASSWORD My1Chosen2Password3;
```

For information on how to backup and restore the encryption root key store (instance SSFS or local secure store (LSS)) by using the hdbnsutil utility, see the SAP HANA Administration Guide.

## Related Information

ALTER SYSTEM VALIDATE ENCRYPTION ROOT KEYS BACKUP PASSWORD Statement (System Management) [→](ALTER-SYSTEM-VALIDATE-ENCRYPTION-ROOT-KEYS-BACKUP-PASSWORD.md) M_PERSISTENCE_ENCRYPTION_KEYS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_PERSISTENCE_ENCRYPTION_KEYS-System-View.md) ALTER SYSTEM LOG ENCRYPTION Statement (System Management) [→](ALTER-SYSTEM-LOG-ENCRYPTION-Statement-System-Management.md) ALTER SYSTEM BACKUP ENCRYPTION Statement (System Management) [→](ALTER-SYSTEM-BACKUP-ENCRYPTION-Statement-System-Management.md) ALTER SYSTEM APPLICATION ENCRYPTION Statement (System Management) [→](ALTER-SYSTEM-APPLICATION-ENCRYPTION-Statement-System.md) ALTER SYSTEM PERSISTENCE ENCRYPTION Statement (System Management) [→](ALTER-SYSTEM-PERSISTENCE-ENCRYPTION-Statement-System.md) ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS Function (Security) [→](../../../4.09-SQL-Functions/4.09.01-Functions-A-Z/ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS-Function-Security.md) ENCRYPTION_ROOT_KEYS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/ENCRYPTION_ROOT_KEYS-System-View.md) APPLICATION_ENCRYPTION_KEYS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/APPLICATION_ENCRYPTION_KEYS-System-View.md) M_ENCRYPTION_OVERVIEW System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_ENCRYPTION_OVERVIEW-System-View.md) BACKUP ENCRYPTION ROOT KEYS Statement (Backup and Recovery) [→](../BACKUP-ENCRYPTION-ROOT-KEYS-Statement-Backup-and-Recovery.md) RECOVER ENCRYPTION ROOT KEYS Statement (Backup and Recovery) [→](../RECOVER-ENCRYPTION-ROOT-KEYS-Statement-Backup-and-Recovery.md)
