# 4.9.1.75 ENCRYPTION_ROOT_KEYS_EXTRACT_ALL_KEYS_FOR_DATABASE Function (Security)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 183–185

Extracts all the encryption root keys of a database and sends them to a client session as a CLOB.

## Syntax

```sql
ENCRYPTION_ROOT_KEYS_EXTRACT_ALL_KEYS_FOR_DATABASE('<database_name>')
```

## Syntax Elements

#### database_name

Specifies the name of the database whose root keys are included in the CLOB. All versions of all key types are included in the CLOB.

## Description

The root keys of a tenant database can be extracted using this function either in the tenant database (in which case the database name is still mandatory), or in the system database if the system database has encryption configuration control for the tenant database. The returned root key backup is base64 encoded and therefore compatible to the CLOB data type. It always contains all root keys for all root key types (that is: DPAPI, BACKUP, LOG, PERSISTENCE).

The returned backup file format depends on the used secure store (local secure store or secure store in the file system).

## Permissions

You must have the `ENCRYPTION ROOT KEY ADMIN` system privilege and the encryption root key backup password must be set.

## Example

The following statement extracts all root keys from the key store and sends them to a client session as a CLOB.

```sql
SELECT ENCRYPTION_ROOT_KEYS_EXTRACT_ALL_KEYS_FOR_DATABASE (‘my_database’) FROM
DUMMY;
```

## Related Information

ALTER SYSTEM VALIDATE ENCRYPTION ROOT KEYS BACKUP PASSWORD Statement (System Management) [→](../../4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-VALIDATE-ENCRYPTION-ROOT-KEYS-BACKUP-PASSWORD.md) ALTER SYSTEM SET ENCRYPTION ROOT KEYS BACKUP PASSWORD Statement (System Management) [→](../../4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-SET-ENCRYPTION-ROOT-KEYS-BACKUP-PASSWORD.md) M_PERSISTENCE_ENCRYPTION_KEYS System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_PERSISTENCE_ENCRYPTION_KEYS-System-View.md) ALTER SYSTEM BACKUP ENCRYPTION Statement (System Management) [→](../../4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-BACKUP-ENCRYPTION-Statement-System-Management.md) ALTER SYSTEM LOG ENCRYPTION Statement (System Management) [→](../../4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-LOG-ENCRYPTION-Statement-System-Management.md) ALTER SYSTEM PERSISTENCE ENCRYPTION Statement (System Management) [→](../../4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-PERSISTENCE-ENCRYPTION-Statement-System.md) ENCRYPTION_ROOT_KEYS System View [→](../../../6-System-Views-Reference/6.01-System-Views/ENCRYPTION_ROOT_KEYS-System-View.md) APPLICATION_ENCRYPTION_KEYS System View [→](../../../6-System-Views-Reference/6.01-System-Views/APPLICATION_ENCRYPTION_KEYS-System-View.md) M_ENCRYPTION_OVERVIEW System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_ENCRYPTION_OVERVIEW-System-View.md)
