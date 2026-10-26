# 4.10.1.19.18 ALTER SYSTEM BACKUP ENCRYPTION Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 501–503

Controls whether data and log backups are stored on disk in an encrypted or non-encrypted format and manages the encryption root keys used.

## Syntax

```sql
ALTER SYSTEM BACKUP ENCRYPTION <encrypt_option>
```

## Syntax Elements

#### encrypt_option

Specifies backup encryption options.

```sql
<encrypt_option> ::=
 CREATE NEW ROOT KEY WITHOUT ACTIVATE
 | ACTIVATE NEW ROOT KEY
 | ON
 | OFF
```

##### CREATE NEW ROOT KEY WITHOUT ACTIVATE

Creates a new random encryption root key for backup encryption with the key state PREACTIVE. Once activated, the new key is used to encrypt any new backups. You must backup the key before it is used to encrypt new backups.

Execute this syntax in the database for which the root key is being created.

An error occurs if a PREACTIVE key already exists and an ALTER SYSTEM BACKUP ENCRYPTION CREATE NEW ROOT KEY WITHOUT ACTIVATE statement is executed. Similarly, an error occurs when a PREACTIVE key does not exist and an ALTER SYSTEM BACKUP ENCRYPTION ACTIVATE NEW ROOT KEY statement is executed.

You must back up the root key store between creating and activating a new root key. You can back up the root key store using BACKUP ENCRYPTION ROOT KEYS or the functions ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS and ENCRYPTION_ROOT_KEYS_EXTRACT_ALL_KEYS_FOR_DATABASE function and saving the results to a backup file.

##### ACTIVATE NEW ROOT KEY

Updates the state of the PREACTIVE root key to ACTIVE, and the previously ACTIVE root key to DEACTIVATED. Once activated, the new key is used for encrypting any new backups. **ON** Turns on backup encryption. Any new backups created after backup encryption is enabled are encrypted using the ACTIVE backup encryption root key. **OFF** Turns off backup encryption. Any new backups created after backup encryption is turned off are written in cleartext. Existing backups remain encrypted.

## Description

You can use this statement to enable or disable backup encryption, and create and activate encryption root keys.

If there is no encryption configuration in the root key store (instance SSFS or LSS), then encryption is interpreted as OFF.

Execute this statement on the database where you want the encryption option to take effect.

> **Note**
>
> If the system database has encryption configuration control, data volume encryption can only be enabled or disabled in a tenant database from the system database using ALTER DATABASE `<database_name>` BACKUP ENCRYPTION ON.

For more information about encryption in the SAP HANA database and the root key change process, see the SAP HANA Security Guide and the SAP HANA Administration Guide.

## Permissions

You must have the ENCRYPTION ROOT KEY ADMIN privilege to execute this statement.

## Example

Create a new backup root key in the preactive state:

```sql
ALTER SYSTEM BACKUP ENCRYPTION CREATE NEW ROOT KEY WITHOUT ACTIVATE;
```

## Related Information

ALTER SYSTEM VALIDATE ENCRYPTION ROOT KEYS BACKUP PASSWORD Statement (System Management) [→](ALTER-SYSTEM-VALIDATE-ENCRYPTION-ROOT-KEYS-BACKUP-PASSWORD.md) M_PERSISTENCE_ENCRYPTION_KEYS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_PERSISTENCE_ENCRYPTION_KEYS-System-View.md) ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS Function (Security) [→](../../../4.09-SQL-Functions/4.09.01-Functions-A-Z/ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS-Function-Security.md) ALTER DATABASE Statement (Tenant Database Management) [→](../ALTER-DATABASE-Statement-Tenant-Database-Management.md) ALTER SYSTEM SET ENCRYPTION ROOT KEYS BACKUP PASSWORD Statement (System Management) [→](ALTER-SYSTEM-SET-ENCRYPTION-ROOT-KEYS-BACKUP-PASSWORD.md) ALTER SYSTEM PERSISTENCE ENCRYPTION Statement (System Management) [→](ALTER-SYSTEM-PERSISTENCE-ENCRYPTION-Statement-System.md) ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS Function (Security) [→](../../../4.09-SQL-Functions/4.09.01-Functions-A-Z/ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS-Function-Security.md) ENCRYPTION_ROOT_KEYS_EXTRACT_ALL_KEYS_FOR_DATABASE Function (Security) [→](../../../4.09-SQL-Functions/4.09.01-Functions-A-Z/ENCRYPTION_ROOT_KEYS_EXTRACT_ALL_KEYS_FOR_DATABASE-Function.md) ENCRYPTION_ROOT_KEYS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/ENCRYPTION_ROOT_KEYS-System-View.md)

APPLICATION_ENCRYPTION_KEYS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/APPLICATION_ENCRYPTION_KEYS-System-View.md) M_ENCRYPTION_OVERVIEW System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_ENCRYPTION_OVERVIEW-System-View.md) ALTER SYSTEM LOG ENCRYPTION Statement (System Management) [→](ALTER-SYSTEM-LOG-ENCRYPTION-Statement-System-Management.md) BACKUP ENCRYPTION ROOT KEYS Statement (Backup and Recovery) [→](../BACKUP-ENCRYPTION-ROOT-KEYS-Statement-Backup-and-Recovery.md) RECOVER ENCRYPTION ROOT KEYS Statement (Backup and Recovery) [→](../RECOVER-ENCRYPTION-ROOT-KEYS-Statement-Backup-and-Recovery.md)
