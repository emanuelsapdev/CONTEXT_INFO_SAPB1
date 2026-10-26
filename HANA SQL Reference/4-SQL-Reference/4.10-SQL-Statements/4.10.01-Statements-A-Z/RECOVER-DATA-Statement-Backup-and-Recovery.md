# 4.10.1.128 RECOVER DATA Statement (Backup and Recovery)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1000–1004

Recovers the SAP HANA database using a specific data backup.

## Syntax

```sql
RECOVER DATA [ FOR <database_name> ]
 [ <system_source_definition> ]
 <backup_definition_for_recovery>
 CLEAR LOG
 [ <additional_option_list> ]
 [ <ignore_option> ]
```

## Syntax Elements

#### database_name

Working from the system database, this option specifies the tenant database to be recovered.

```sql
<database_name> ::= FOR <identifier>
```

If no database name is specified, the local database is assumed.

#### system_source_definition

For third-party backup tools, identifies the source system that was used to create the backups.

This option can only be used in combination with `USING BACKINT`.

```sql
<system_source_definition> ::= USING SOURCE '<system_id>'
```

`USING SOURCE` specifies that the data backup is of a database with a different SID or name than the target system.

For example, if you are recovering the system database for system PR1, the statement would be as follows:

```sql
<system_source_definition> ::= USING SOURCE 'SYSTEMDB@PR1'
```

To recover a tenant database using a Backint-based backup that was created in a system identified by the system ID PR1 and the name `Tenant_1`, the option would be:

```sql
<system_source_definition> ::= USING SOURCE 'Tenant_1@PR1'
```

To recover a Backint-based data backup from a single container system identified by the system ID PR1, use the following option:

```sql
USING SOURCE 'PR1'
```

#### backup_definition_for_recovery

Specifies recovery settings for the backup.

```sql
<backup_definition_for_recovery> ::=
 USING FILE ('<prefix>')
 | USING BACKINT ('<prefix>')
 | USING SNAPSHOT
 | USING BACKUP_ID <backup_id> [ <catalog_data_path_definition> ]
<catalog_data_path_definition> ::=
 USING CATALOG BACKINT
 | USING CATALOG PATH (<'path'>) ] [ USING DATA PATH (<'path_list'>) ]
```

`USING SNAPSHOT` recovers the database from a data snapshot.

> **Note**
>
> You can recover SAP HANA using a data snapshot of an SAP HANA database with one or more tenant databases. When you recover SAP HANA from a data snapshot, you need to recover **both** the system database and each tenant database separately.

`USING BACKUP_ID` specifies the ID of the full data backup to use for recovery.

`<backup_definition_for_recovery>` can point to either the file system or to a third-party backup tool. An SQL statement can have either `USING CATALOG BACKINT` or `USING CATALOG PATH`, but not both.

`USING CATALOG BACKINT` specifies that the location of the backup catalog is a third-party backup tool.

`USING CATALOG PATH` specifies that the location of the backup catalog is in the file system.

An SQL statement can have either `USING CATALOG BACKINT` or `USING CATALOG PATH`, but not both.

To use a backup catalog that is in a third-party backup tool, use the option `USING CATALOG BACKINT`. When a backup catalog in a third-party backup tool is accessed, only the configured location is accessed. No traversal search for a backup catalog is done. You can specify a particular data backup using the `BACKUP_ID` option.

In the file system, SAP HANA searches the specified locations for the backup catalog in the following order:

| **Path Specified...** | **Where Searched...** |
| --- | --- |
| 1.<br>In the SQL statement (optional):<br> `USING CATALOG PATH` | The path specified is searched for a backup catalog.<br>No subdirectories are searched. |
| 2.<br>Configured path. | The path to be searched is specified by the following parameter:<br> `basepath_catalogbackup`<br>This parameter is in the `persistence` section of the `global.ini` parameter file. |

`USING DATA PATH` is an additional option for `USING CATALOG PATH`. `USING DATA PATH` specifies the location of the data backup in the file system.

In the file system, SAP HANA searches the specified locations for backups in the following order:

| **Path Specified...** | **Where Searched...** |
| --- | --- |
| 1.<br>In the SQL statement (optional):<br> `USING DATA PATH <path list>` | The specified paths are searched for data backups or log backups.<br>All subdirectories are searched.<br>If a specified path is **relative**, the path is based on the backup paths specified by the following parameters:<br> `basepath_databackup`<br>This parameter is in the `persistence` section of the `global.ini` parameter file. |
| 2.<br>Configured paths. | The paths to be searched are specified by the following parameters:<br> `basepath_databackup`<br>Theis parameter is in the `persistence` section of the `global.ini` parameter file. |
| 3.<br>If no backups are found in the paths for 1. or 2. | The paths specified in the original backup catalog are searched for the backups. |

#### CLEAR LOG

The `CLEAR LOG` option **must be used** here to prevent entries from the log area from being used for the recovery. No log entries from the log area are replayed, and the log area is initialized. As a consequence, the content of the log area is lost.

#### additional_option_list

Additional options for recovery.

```sql
<additional_option_list> ::= <additional_option> [...]
```

```sql
<additional_option> ::= SET LICENSE '<license>' | TOOLOPTION
'<parameter_string>'
```

`SET LICENSE` allows you to set the license during the recovery.

`TOOLOPTION` is only available for BACKINT. `TOOLOPTION` passes a vendorspecific parameter string to a third-party backup tool. The string has a maximum length of 4096 bytes.

#### ignore_option_list

```sql
<ignore_option_list> ::= <ignore_option> [...]
```

```sql
<ignore_option> ::= IGNORE WORKERGROUPS | IGNORE COMPATIBILITY CHECK
```

`IGNORE WORKERGROUPS`: By default, when you recover a database from an indexserver that has worker groups, the target system must have worker groups with the same names as in the source system. Otherwise, the recovery fails. `IGNORE WORKERGROUPS` removes this restriction. If worker groups with matching names are found on the target system, they are used. If no worker groups with matching names are found, the worker groups of the backup service are changed to the default to match those of the target system.

`IGNORE COMPATIBILITY CHECK`: By default, the version of the backup is checked for compatibility with the SAP HANA revision. You have the option to recover SAP HANA without performing this check.

> **Caution**
>
> Disabling the compatibility check may have unforeseen consequences. Use this option only in exceptional situations.

For more information, see SAP Note 1948334 (SAP HANA Database Update Paths for SAP HANA Maintenance Revisions)

## Description

The database is recovered to the state of the full backup.

Incremental, differential, and log backups are ignored. No log entries from the log area are replayed, and the log area is initialized. As a consequence, the content of the log area is lost.

After the recovery, the SAP HANA database is online and can be used by applications.

## Permissions

Privilege needed:

`FOR <database_name>`: DATABASE RECOVERY OPERATOR or DATABASE ADMIN

## Examples

### Scenario 1: Recover Without Replaying the Redo Log

In this example, the data backup is taken from the specified directory `/backup`, and has the backup prefix THURSDAY. No log entries from the log area are replayed, and the log area is initialized.

```sql
RECOVER DATA USING FILE ('/backup/THURSDAY') CLEAR LOG;
```

### Scenario 2: Copy a Tenant Database from a Third-Party Backup Tool

In this example, a source tenant database named `Tenant_0` is copied using a Backint-based data backup to a target tenant database named `Tenant_1`. The Backint-based data backup is stored in a third-party backup tool that is identified by the source system ID (SID) (in this example, PR1) and the tenant database name `Tenant_0`. The Backint-based data backup name is specified by a backup prefix (in this example, the timestamp for Thursday, November 26, 2020 at 9 a.m.).

```sql
RECOVER DATA FOR Tenant_1 USING SOURCE 'Tenant_0@PR1' USING
BACKINT('2020-11-26') CLEAR LOG;
```

### Scenario 3: Recover Using a Backup in the File System and a Backup Catalog in a Third- Party Backup Tool

In this example, a tenant database `PR2` in SAP HANA system `PR2` is recovered using a data backup of tenant database `PR1` in SAP HANA system `PR1`. The data backup of `PR1` has BACKUP_ID `1591709192198`. The backup catalog is in a third-party backup tool. The data backup was created in the file system of the source system, and was copied to the file system of the target system. `USING DATA PATH` is used to override the path specified in the source backup catalog with the file system directory that currently contains the data backup.

```sql
RECOVER DATA FOR PR2 USING SOURCE 'PR1@PR1' USING BACKUP_ID 1591709192198 USING
DATA PATH ('/hana/PR1/backup/data') CLEAR LOG
```

### Scenario 4: Recover Using a Backup in a Third-Party Backup Tool and a Backup Catalog in the File System

In this example, a tenant database `PR2` in SAP HANA system `PR2` is recovered using a data backup of tenant database `PR1` in SAP HANA system `PR1`. The data backup of `PR1` is in a third-party backup tool and has BACKUP_ID `1591709192198`. The backup catalog is in the file system of the target system. For this reason, `USING CATALOG PATH` is used to specify the location of the backup catalog to be used.

```sql
RECOVER DATA FOR PR2 USING SOURCE 'PR1@PR1' USING BACKUP_ID 1591709192198 USING
CATALOG PATH ('/hana/PR1/backup/catalog') CLEAR LOG
```

## Related Information

SAP Note 1948334
