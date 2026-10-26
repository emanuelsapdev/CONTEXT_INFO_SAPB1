# 4.10.1.32 BACKUP CHECK ACCESS Statement (Backup and Recovery)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 661–663

Checks whether a backup can be accessed, and the integrity of its metadata.

## Syntax

```sql
BACKUP CHECK ACCESS [<for_database>] BACKUP_ID <int_const>
   [<system_source_definition>] [<path_definition>]
```

## Syntax Elements

#### for_database

Checks if a specified backup can be accessed by the tenant database.

```sql
<for_database> ::= FOR <database_name>
```

This command is only available for SAP HANA tenant databases.

#### int_const

Specifies the BACKUP ID of the full data backup to use for recovery.

For example, `BACKUP_ID 1540499452637`.

#### system_source_definition

```sql
<system_source_definition> ::=
 USING SOURCE '<system_id>'
```

#### path_definition

```sql
<path_definition> ::=
 [USING CATALOG PATH ( <path> )]
 [USING LOG PATH ( <path_list> )]
 [USING DATA PATH ( <path> )]
<path_list> ::=
 '<path>'| <path_list> , '<path>'
```

In the file system, SAP HANA searches the specified locations for the backup catalog in the following order:

| **Path Specified...** | **Where Searched...** |
| --- | --- |
| 1.<br>In the SQL statement (optional):<br> `USING CATALOG PATH` | The path specified is searched for a backup catalog.<br>No subdirectories are searched. |
| 2.<br>Configured path. | The path to be searched is specified by the following parameter:<br> `basepath_catalogbackup`<br>This parameter is in the `persistence` section of the `global.ini` parameter file. |

In the file system, SAP HANA searches the specified locations for backups in the following order:

| **Path Specified...** | **Where Searched...** |
| --- | --- |
| 1.<br>In the SQL statement (optional):<br> `USING LOG PATH <path list> USING DATA PATH <path>` | The specified paths are searched for data backups or log backups.<br>All subdirectories are searched.<br>If a specified path is **relative**, the path is based on the backup paths specified by the following parameters:<br> `basepath_databackup basepath_logbackup`<br>These parameters are in the `persistence` section of the `global.ini` parameter file. |
| 2.<br>Configured paths. | The paths to be searched are specified by the following parameters:<br> `basepath_databackup basepath_logbackup`<br>These parameters are in the `persistence` section of the `global.ini` parameter file. |
| 3.<br>If no backups are found in the paths for 1. or 2. | The paths specified in the original backup catalog are searched for the backups. |

## Description

This statement checks whether a backup can be accessed, and the integrity of its metadata.

`BACKUP CHECK ACCESS` only checks an individual backup. Conversely, the `CHECK ACCESS` option for `RECOVER DATABASE` checks whether all the backups required for a recovery are available.

### hdbbackupdiag

`BACKUP CHECK ACCESS` performs the same function as the `--check` option of `hdbbackupdiag`. However, with `BACKUP CHECK ACCESS`, the database must be offline. With `hdbbackupdiag`, the database can be either offline or online.

`BACKUP CHECK ACCESS` only checks for a single complete data backup identified by a specific backup ID. `BACKUP CHECK ACCESS` does not check for log backups or delta backups.

`hdbbackupdiag --check` checks whether all the backups (including log backups and delta backups) required for a recovery exist and can be accessed, and also that the metadata is consistent.

Unlike `hdbbackupdiag --check`, the `hdbbackupcheck` tool checks the content of the backups on page level using checksums.

For more information about `hdbbackupcheck`, see SAP Note 1869119 (Checking backups with "hdbbackupcheck").

### Error Handling

The result set of `BACKUP CHECK ACCESS` is written to an XML file named `strategyOutput.xml` in the SAP HANA trace directory.

`BACKUP CHECK ACCESS` only reports an error to the client if there is a syntax error, or if an incorrect system source definition was specified.

If no result set is returned, `strategyOutput.xml` is not changed.

An SQL error is not always returned. If `strategyOutput.xml` was not created or was rewritten, check the `backup.log` for error messages.

For more information, see backup.log in the SAP HANA Administration Guide (SAP HANA Database Backup and Recovery).

## Permissions

Privilege needed:

`FOR <database_name>`: DATABASE RECOVERY OPERATOR or DATABASE ADMIN

## Related Information

SAP Note 1869119 backup.log (SAP HANA Administration Guide (SAP HANA Database Backup and Recovery))
