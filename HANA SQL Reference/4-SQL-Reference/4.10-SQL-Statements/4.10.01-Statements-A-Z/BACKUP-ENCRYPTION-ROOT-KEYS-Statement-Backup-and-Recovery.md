# 4.10.1.37 BACKUP ENCRYPTION ROOT KEYS Statement (Backup and Recovery)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 673–676

This statement allows you to back up the root keys for the system database or a tenant database.

## Syntax

```sql
BACKUP ENCRYPTION ROOT KEYS [ <root_keytype_list> ] [ FOR <database_name> ]
USING <root_key_backup_definition_file>
```

## Syntax Elements

#### root_keytype_list ::= root_keytype [, root_keytype_list ]

Specifies the root key type.

If `<root_keytype_list>` is specified:

| SSFS: | `<root_keytype_list>` can be used without any restrictions. |
| --- | --- |
| LSS with an active key management system: | • `<root_keytype_list>` is refused.<br>• If the system is not connected to a key management system, a root keys backup (in the old format) is created.<br>• Otherwise, an error is returned. |

If a `<root_keytype_list>` is not specified, a full Secure Store backup is created.

If SSFS is used, the backup is in an SSFSspecific format. If LSS is used, an LSS backup is created. SSFS backups can be recovered to a system that is using LSS.

#### database_name

Specifies the name of the tenant database.

To back up the root keys for the system database, `FOR <database_name>` does not need to be specified.

#### root_keytype ::= PERSISTENCE | APPLICATION | BACKUP | LOG

`<root_keytype>` can be PERSISTENCE, APPLICATION, BACKUP, or LOG, or a combination of them. If a `<root_keytype>` is not specified, all encryption root key types are backed up.

#### root_key_backup_definition_file ::= FILE ( 'prefix' | 'path', 'prefix' )

Specifies the root key backup definition file. The file is written to the file system on the database back-end.

The name of the backup file is constructed from the following elements: `<prefix>_<database_name>_rootkeys`

If `<path>` is not specified, SAP HANA attempts to retrieve the backup location from the configuration parameter `<basepath_rootkeybackup>` in the `<persistence>` section of the `global.ini` file.

If the `basepath_rootkeybackup` parameter is not configured, the default backup path `$ {DIR_INSTANCE}/backup/sec` is used.

## Description

> **Restriction**
>
> This statement can only be used to create encryption root key backups in the file system.
>
> Use with third-party backup tools is not supported.

The statement must be executed in the system database.

The tenant database can be online or offline.

Before the BACKUP ENCRYPTION ROOT KEYS statement is executed, encryption configuration control must be given to the system database for the tenant database. Use the following SQL statement:

```sql
ALTER SYSTEM ENCRYPTION CONFIGURATION CONTROLLED BY SYSTEM DATABASE
```

> **Note**
>
> If the system database does not own encryption key management control for the tenant database, the statement will fail.

### Backup Password

A password for the backup of encryption root keys must be set **before** the backup is created.

To set a password for the system database, use the following SQL statement on the system database:

```sql
ALTER DATABASE SET ENCRYPTION ROOT KEYS BACKUP PASSWORD <PASSWORD>
```

To set a password for a tenant database, use the following SQL statement from the system database:

```sql
ALTER DATABASE <database_name> SET ENCRYPTION ROOT KEYS BACKUP PASSWORD
<PASSWORD>
```

## Permissions

The use of this statement requires the system privilege ENCRYPTION ROOT KEY ADMIN.

For the **system database**, this statement requires one of the following privileges:

- BACKUP ADMIN
- BACKUP OPERATOR

For a **tenant database**, this statement requires one of the following privileges:

- DATABASE BACKUP ADMIN
- DATABASE BACKUP OPERATOR

Actions on the backup file on operating system level, for example to copy the file to additional locations, require an operating system user.

## Example

```sql
BACKUP ENCRYPTION ROOT KEYS USING FILE ('/backup/HDB/rootkeys/backup001')
```

Backs up encryption root keys (all key types) for the system database. (FOR `<DATABASE_NAME>` is omitted.)

```sql
BACKUP ENCRYPTION ROOT KEYS FOR testDB USING FILE (‘backup001’)
```

Backs up all encryption root keys for the tenant database `testDB`. The prefix is `backup001`.

A backup file is generated with the name: `backup001_testDB_rootkeys`

## Related Information

RECOVER ENCRYPTION ROOT KEYS Statement (Backup and Recovery) [→](RECOVER-ENCRYPTION-ROOT-KEYS-Statement-Backup-and-Recovery.md) ALTER SYSTEM SET ENCRYPTION ROOT KEYS BACKUP PASSWORD Statement (System Management) [→](4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-SET-ENCRYPTION-ROOT-KEYS-BACKUP-PASSWORD.md) ALTER SYSTEM BACKUP ENCRYPTION Statement (System Management) [→](4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-BACKUP-ENCRYPTION-Statement-System-Management.md) Back Up Root Keys Root Key Backup
