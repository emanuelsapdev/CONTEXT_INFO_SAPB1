# 4.9.1.73 ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS Function (Security)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 181–183

Extracts root keys and sends them to a client session as a CLOB.

## Syntax

```sql
ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS(['<root_keytype_list>'])
```

## Syntax Elements

#### root_keytype_list

Specify the key types that are included in the CLOB. All versions of the specified key type are included in the CLOB. If `<root_keytype_list>` is empty, then all key types are included in the CLOB.

```sql
<root_keytype_list> ::=
 <root_keytype> [, ...]
<root_keytype> ::=
 PERSISTENCE | APPLICATION | LOG | BACKUP
```

**PERSISTENCE** The following statement extracts all persistence and log root keys from the encryption rootSpecifies that persistence encryption root keys are extracted. **APPLICATION** Specifies that application encryption root keys are extracted. **LOG** Specifies that log encryption root keys are extracted.

**BACKUP** Specifies that backup encryption root keys are extracted.

## Description

Execute this statement in the database from which the root keys are being extracted.

## Permissions

You must have the ENCRYPTION ROOT KEY ADMIN privilege and the encryption root key backup password should be set in the encryption root key store (instance SSFS or local secure store (LSS)).

## Example

The following statement extracts all persistence and log root keys from the encryption root key store (instance SSFS) and sends them to a client session as a CLOB.

```sql
SELECT ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS ('PERSISTENCE, LOG') FROM DUMMY;
```

The following statement includes all key types in the CLOB.

```sql
SELECT ENCRYPTION_ROOT_KEYS_EXTRACT_KEYS ('') FROM DUMMY;
```

## Related Information

ALTER SYSTEM VALIDATE ENCRYPTION ROOT KEYS BACKUP PASSWORD Statement (System Management) [→](../../4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-VALIDATE-ENCRYPTION-ROOT-KEYS-BACKUP-PASSWORD.md) ALTER SYSTEM BACKUP ENCRYPTION Statement (System Management) [→](../../4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-BACKUP-ENCRYPTION-Statement-System-Management.md) M_PERSISTENCE_ENCRYPTION_KEYS System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_PERSISTENCE_ENCRYPTION_KEYS-System-View.md) ALTER SYSTEM SET ENCRYPTION ROOT KEYS BACKUP PASSWORD Statement (System Management) [→](../../4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-SET-ENCRYPTION-ROOT-KEYS-BACKUP-PASSWORD.md) ALTER SYSTEM LOG ENCRYPTION Statement (System Management) [→](../../4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-LOG-ENCRYPTION-Statement-System-Management.md) ALTER SYSTEM PERSISTENCE ENCRYPTION Statement (System Management) [→](../../4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-PERSISTENCE-ENCRYPTION-Statement-System.md) ENCRYPTION_ROOT_KEYS System View [→](../../../6-System-Views-Reference/6.01-System-Views/ENCRYPTION_ROOT_KEYS-System-View.md) APPLICATION_ENCRYPTION_KEYS System View [→](../../../6-System-Views-Reference/6.01-System-Views/APPLICATION_ENCRYPTION_KEYS-System-View.md) M_ENCRYPTION_OVERVIEW System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_ENCRYPTION_OVERVIEW-System-View.md)
