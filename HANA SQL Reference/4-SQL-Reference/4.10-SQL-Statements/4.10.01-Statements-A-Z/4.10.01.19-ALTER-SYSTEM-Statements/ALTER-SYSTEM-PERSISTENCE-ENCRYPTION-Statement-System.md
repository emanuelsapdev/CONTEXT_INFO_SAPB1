# 4.10.1.19.36 ALTER SYSTEM PERSISTENCE ENCRYPTION Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 524–527

Controls whether persistent data is stored on disk in an encrypted or non-encrypted format and manages the page encryption keys and encryption root keys used.

## Syntax

```sql
ALTER SYSTEM PERSISTENCE ENCRYPTION <encrypt_option>
```

## Syntax Elements

#### encrypt_option

Specifies encryption options.

```sql
<encrypt_option> ::=
 | CREATE NEW KEY
 | APPLY CURRENT KEY
 | CREATE NEW ROOT KEY [WITHOUT ACTIVATE]
 | ACTIVATE NEW ROOT KEY
 | ON
 | OFF
```

##### CREATE NEW KEY

Creates a new random page encryption key. The new key is used to encrypt any pages written to disk during subsequent savepoint operations. The time required for this operation depends on the current workload of the SAP HANA database. No changes are made to data that has already been written to disk.

##### APPLY CURRENT KEY

Forces all data using old page encryption keys to be decrypted and then re-encrypted using the current page encryption key. You may wish to do this if an old key has been compromised or if you want to consolidate a set of old keys.

When new key has been created with CREATE NEW KEY and then APPLY CURRENT KEY is called, a savepoint is automatically triggered so that the new key is used to encrypt and save any in-memory pages.

##### CREATE NEW ROOT KEY [WITHOUT ACTIVATE]

Creates a new random encryption root key.

Specifying WITHOUT ACTIVATE creates a new version of the root key with the key state PREACTIVE. If a preactive key already exists, then an error occurs. If you do not specify WITHOUT ACTIVATE, then the specified key is created and activated. The new key is used for re-encrypting all page encryption keys after the next savepoint occurs. The point in time for the next savepoint is influenced by the current workload in the database. **ACTIVATE NEW ROOT KEY** Updates the state of the PREACTIVE root key to ACTIVE, and the previously ACTIVE root key to DEACTIVATED. Once activated, the new key is used for re-encrypting all page encryption keys after the next savepoint occurs. The point in time for the next savepoint is influenced by the current workload in the database.

##### ON

Specifies that encryption of data volumes should be enabled. When you switch on encryption, a random encryption key is prepared and an asynchronous background task is started that encrypts all disk data with this key. **OFF** Specifies that encryption of data volumes should be disabled. When you switch off encryption, an asynchronous background task is started which decrypts all encrypted disk data.

## Description

You can use this statement to enable or disable log volume encryption, create and apply new random page encryption keys, and create and activate encryption root keys.

Execute this statement on the database where you want the encryption option to take effect.

> **Note**
>
> If the system database has encryption configuration control, data volume encryption can only be enabled or disabled in a tenant database from the system database using ALTER DATABASE `<database_name>` PERSISTENCE ENCRYPTION ON.

Only the finally written disk data is encrypted. The redo log is not affected by this command.

For more information about encryption in the SAP HANA database, see the SAP HANA Security Guide and the SAP HANA Administration Guide.

You must back up the root key store between creating and activating a new root key. You can back up the root key store using BACKUP ENCRYPTION ROOT KEYS or the functions ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS and ENCRYPTION_ROOT_KEYS_EXTRACT_ALL_KEYS_FOR_DATABASE function and saving the results to a backup file.

Always back up your root keys before you enable encryption.

For more information about encryption in the SAP HANA database and the root key change process, see the SAP HANA Security Guide and the SAP HANA Administration Guide.

If there is no encryption configuration in the root key store (instance SSFS or LSS), then encryption is interpreted as OFF.

## Permissions

You must have the ENCRYPTION ROOT KEY ADMIN or RESOURCE ADMIN privilege to create or apply page encryption keys. You must have the ENCRYPTION ROOT KEY ADMIN privilege to create and activate root keys and to enable and disable encryption.

## Example

1. Create a new data volume encryption root key in the preactive state.

```sql
ALTER SYSTEM PERSISTENCE ENCRYPTION CREATE NEW ROOT KEY WITHOUT ACTIVATE;
```

2. Cause a non-encrypted instance to begin the asynchronous task of encrypting disk data.

```sql
ALTER SYSTEM PERSISTENCE ENCRYPTION ON;
```

## Related Information

ALTER SYSTEM VALIDATE ENCRYPTION ROOT KEYS BACKUP PASSWORD Statement (System Management) [→](ALTER-SYSTEM-VALIDATE-ENCRYPTION-ROOT-KEYS-BACKUP-PASSWORD.md) ALTER SYSTEM LOG ENCRYPTION Statement (System Management) [→](ALTER-SYSTEM-LOG-ENCRYPTION-Statement-System-Management.md) ALTER SYSTEM BACKUP ENCRYPTION Statement (System Management) [→](ALTER-SYSTEM-BACKUP-ENCRYPTION-Statement-System-Management.md) ALTER SYSTEM APPLICATION ENCRYPTION Statement (System Management) [→](ALTER-SYSTEM-APPLICATION-ENCRYPTION-Statement-System.md) ALTER DATABASE Statement (Tenant Database Management) [→](../ALTER-DATABASE-Statement-Tenant-Database-Management.md) M_PERSISTENCE_ENCRYPTION_KEYS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_PERSISTENCE_ENCRYPTION_KEYS-System-View.md) ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS Function (Security) [→](../../../4.09-SQL-Functions/4.09.01-Functions-A-Z/ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS-Function-Security.md) ENCRYPTION_ROOT_KEYS_EXTRACT_ALL_KEYS_FOR_DATABASE Function (Security) [→](../../../4.09-SQL-Functions/4.09.01-Functions-A-Z/ENCRYPTION_ROOT_KEYS_EXTRACT_ALL_KEYS_FOR_DATABASE-Function.md) BACKUP ENCRYPTION ROOT KEYS Statement (Backup and Recovery) [→](../BACKUP-ENCRYPTION-ROOT-KEYS-Statement-Backup-and-Recovery.md) ALTER SYSTEM SET ENCRYPTION ROOT KEYS BACKUP PASSWORD Statement (System Management) [→](ALTER-SYSTEM-SET-ENCRYPTION-ROOT-KEYS-BACKUP-PASSWORD.md) ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS Function (Security) [→](../../../4.09-SQL-Functions/4.09.01-Functions-A-Z/ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS-Function-Security.md) ENCRYPTION_ROOT_KEYS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/ENCRYPTION_ROOT_KEYS-System-View.md) APPLICATION_ENCRYPTION_KEYS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/APPLICATION_ENCRYPTION_KEYS-System-View.md) M_ENCRYPTION_OVERVIEW System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_ENCRYPTION_OVERVIEW-System-View.md)
