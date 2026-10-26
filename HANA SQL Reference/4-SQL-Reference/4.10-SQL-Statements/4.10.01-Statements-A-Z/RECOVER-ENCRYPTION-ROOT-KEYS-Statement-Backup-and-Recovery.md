# 4.10.1.130 RECOVER ENCRYPTION ROOT KEYS Statement (Backup and Recovery)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1012–1015

This statement allows you to recover the encryption root keys for a tenant database. To recover the encryption root keys for a system database, use the `hdbnsutil` tool.

## Syntax

```sql
RECOVER ENCRYPTION ROOT KEYS [ AND SETTINGS | (<root_keytype_list>) ] FOR
<database_name> USING FILE <root_key_backup_definition_file> PASSWORD <password>
[ SECURE STORE SECOND ACCESS (<PRIVATE KEY 'KEY'> <PASSWORD 'PWD'> [ CERTIFICATE
'CERT' ]) ]
```

## Syntax elements

#### AND SETTINGS

`AND SETTINGS` recovers the full LSS backup. This includes keys, key management configuration, encryption control, and encryption settings.

> **Caution**
>
> `AND SETTINGS` replaces the current keys. When an encryption root key backup is recovered to a tenant database, any existing encryption root keys for that tenant database will be overwritten.

If `AND SETTINGS` is not specified, only the keys are recovered. The keys from the backup are added, but not replaced.

#### root_keytype_list ::= root_keytype [, root_keytype_list ]

Specifies the root key type.

| SSFS: | `<root_keytype_list>` can be used without any restrictions. |
| --- | --- |
| LSS with an active key management system: | `<root_keytype_list>` is refused. |

If a `<root_keytype_list>` is not specified, all root key types that are stored in the specified file are recovered.

#### database_name

Specifies the name of the tenant database.

#### root_keytype ::= PERSISTENCE | APPLICATION | BACKUP | LOG

`<root_keytype>` can be PERSISTENCE, APPLICATION, BACKUP, or LOG, or a combination of them. If a `<root_keytype>` is not specified, all root key types that are stored in the specified file are recovered.

#### root_key_backup_definition_file ::= FILE ( 'prefix' | 'path', 'prefix' )

Specifies the root key backup definition file in the file system.

The name of the backup file is constructed from the following elements: `<prefix>_<database_name>_rootkeys`

If `<path>` is not specified, SAP HANA attempts to retrieve the backup location from a configuration parameter `<basepath_rootkeybackup>` in the `<persistence>`section of the `global.ini` file.

If the `basepath_rootkeybackup` parameter is not configured, the default backup path `$ {DIR_INSTANCE}/backup/sec` is used.

#### password

The password is set **before** the encryption root key file is backed up.

Using `ALTER SYSTEM SET ENCRYPTION ROOT KEYS BACKUP PASSWORD`, the password is first set and then used during the backup.

For more information, see BACKUP ENCRYPTION ROOT KEYS Statement (Backup and Recovery).

#### SECURE STORE SECOND ACCESS (PRIVATE KEY 'KEY' PASSWORD 'PWD' [ CERTIFICATE 'CERT' ])

Secure store second access is only needed if LSS is used with an active key management system that can no longer be reached.

If the KMS is not available, and a backup is recovered with secure store second access, the recovered database will be recovered **without** restoring the KMS. Consequently, if you require KMS protection, you will need to set it up again.

## Description

> **Restriction**
>
> This statement can only be used to recover encryption root key backups from the file system.
>
> Use with third-party backup tools is not supported.

The statement must be executed in the system database.

To prevent inconsistencies in the persistence layer, the tenant database must be offline.

It does not matter if the system database user (`<sid>adm`) is the owner of the backup file or not.

With LSS, `RECOVER ENCRYPTION ROOT KEYS` supports second access keys. If the connection to the key management system is lost, or the key was deleted, backups can be recovered using the second access key.

> **Note**
>
> Using this statement, the encryption root keys can only be recovered for tenant databases. To recover the encryption root keys for a system database, use the `hdbnsutil` tool.
>
> For more information about the `hdbnsutil` utility, see the SAP HANA Administration Guide.

## Permissions

Privilege needed:

`FOR <database_name>`: DATABASE RECOVERY OPERATOR or DATABASE ADMIN

## Example

```sql
RECOVER ENCRYPTION ROOT KEYS PERSISTENCE FOR testDB USING FILE ('/backup/HDB/
rootkeys/backup001') PASSWORD <PASSWORD>
```

Recovers the encryption root keys for the root key type PERSISTENCE for the `testDB` database from the backup file `/backup/Hs/data/backup001_testDB_rootkeys`.

## Related Information

BACKUP ENCRYPTION ROOT KEYS Statement (Backup and Recovery) [→](BACKUP-ENCRYPTION-ROOT-KEYS-Statement-Backup-and-Recovery.md) ALTER SYSTEM SET ENCRYPTION ROOT KEYS BACKUP PASSWORD Statement (System Management) [→](4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-SET-ENCRYPTION-ROOT-KEYS-BACKUP-PASSWORD.md) ALTER SYSTEM BACKUP ENCRYPTION Statement (System Management) [→](4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-BACKUP-ENCRYPTION-Statement-System-Management.md)
