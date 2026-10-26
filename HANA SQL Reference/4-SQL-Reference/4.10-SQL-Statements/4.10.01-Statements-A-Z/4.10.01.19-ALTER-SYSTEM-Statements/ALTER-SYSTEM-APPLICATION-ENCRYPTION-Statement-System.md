# 4.10.1.19.17 ALTER SYSTEM APPLICATION ENCRYPTION Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 499–501

Manages encryption keys for applications that use the internal data encryption service.

## Syntax

```sql
ALTER SYSTEM APPLICATION ENCRYPTION <encrypt_option>
```

## Syntax Elements

#### encrypt_option

Specifies application encryption options.

```sql
<encrypt_option> ::=
 CREATE NEW KEY
 | CREATE NEW ROOT KEY WITHOUT ACTIVATE
 | ACTIVATE NEW ROOT KEY
```

##### CREATE NEW KEY

Creates a new, random encryption key for every application.

##### CREATE NEW ROOT KEY WITHOUT ACTIVATE

The CREATE NEW ROOT KEY WITHOUT ACTIVATE clause creates a new ACTIVE root key, re-encrypts all application keys using the new key, and records the new key in the redo log.

The new root key is in the PREACTIVE state. A PREACTIVE key is not recorded in the redo log and cannot be used to re-encrypt the application encryption keys. This clause returns an error if a PREACTIVE key already exists. Creating a PREACTIVE application root key allows you to back up the key before using it to encrypt application keys.

##### ACTIVATE NEW ROOT KEY

Activates a PREACTIVE key that was previously created by using the CREATE NEW ROOT KEY WITHOUT ACTIVATE clause. This clause updates the state of the PREACTIVE root key to ACTIVE and the previously ACTIVE root key to DEACTIVATED. An error is returned if a PREACTIVE root key does not exist.

This clause re-encrypts all application keys by using the activated root key.

## Description

You can use this statement to manage random encryption keys for application encryption and create and activate root keys.

Applications are consumers of the internal data encryption service, such as internal components, like the secure internal credential store, or XS applications. The new keys are stored encrypted with the current root key of the internal data encryption service. The new keys are used after the transaction is committed. No changes are made to data that has already been written to disk.

Use this statement if your company's security policies dictate that you should periodically change the encryption keys being used to store your data, or if you are instructed to do so by SAP Support.

You must back up the root key store between creating and activating a new root key. You can back up the root key store by using the ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS function and saving the results in a backup file.

For more information about encryption in the SAP HANA database and the key change process, see the SAP HANA Administration Guide and the SAP HANA Security Guide.

## Permissions

You must have the ENCRYPTION ROOT KEY ADMIN privilege to execute this statement.

You must have the ENCRYPTION ROOT KEY ADMIN or RESOURCE ADMIN privilege to create application encryption keys.

## Example

Create new encryption keys for all applications.

```sql
ALTER SYSTEM APPLICATION ENCRYPTION CREATE NEW KEY;
```

## Related Information

ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS Function (Security) [→](../../../4.09-SQL-Functions/4.09.01-Functions-A-Z/ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS-Function-Security.md) ALTER SYSTEM SET ENCRYPTION ROOT KEYS BACKUP PASSWORD Statement (System Management) [→](ALTER-SYSTEM-SET-ENCRYPTION-ROOT-KEYS-BACKUP-PASSWORD.md) ALTER SYSTEM PERSISTENCE ENCRYPTION Statement (System Management) [→](ALTER-SYSTEM-PERSISTENCE-ENCRYPTION-Statement-System.md) ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS Function (Security) [→](../../../4.09-SQL-Functions/4.09.01-Functions-A-Z/ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS-Function-Security.md) ENCRYPTION_ROOT_KEYS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/ENCRYPTION_ROOT_KEYS-System-View.md) APPLICATION_ENCRYPTION_KEYS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/APPLICATION_ENCRYPTION_KEYS-System-View.md) M_ENCRYPTION_OVERVIEW System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_ENCRYPTION_OVERVIEW-System-View.md) ALTER SYSTEM LOG ENCRYPTION Statement (System Management) [→](ALTER-SYSTEM-LOG-ENCRYPTION-Statement-System-Management.md)
