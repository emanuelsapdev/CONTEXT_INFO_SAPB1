# 4.10.1.38 BACKUP LIST DATA Statement (Backup and Recovery)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 676–678

Uses the backup catalog to generate a list of data backups that can be used to recover SAP HANA to a specified point in time.

## Syntax

```sql
BACKUP LIST DATA [ <for_database> ] <until_definition>
[ <system_source_definition> ] [ <path_definition> ] [ <limit_offset> ]
 | BACKUP COMPLETE LIST DATA [ <for_database> ] [ <system_source_definition> ]
[ <path_definition> ] [ <limit_offset> ]
```

## Syntax Elements

#### for_database

Specifies the backup catalog for a tenant database.

```sql
<for_database> ::= FOR <databasename>
```

For example: `BACKUP LIST DATA FOR DB0 UNTIL TIMESTAMP '2020-10-21'`.

Requirements:

- Executed on the system database only.
- The system database must be online, but the tenant database must be offline.

#### until_definition

Specifies a point, up to which to return a list of data backups from the backup catalog. For example, backups that could be used for a recovery up to a specified point in time.

```sql
<until_definition> ::=
 UNTIL LOG POSITION <log_pos> AT VOLUME <volume_id>
 | UNTIL TIMESTAMP '<timestamp>'
```

#### system_source_definition

Identifies the source system.

This option can only be used for a backup catalog from a third-party backup tool.

```sql
<system_source_definition> ::= USING SOURCE <system_id>
```

#### path_definition

Specifies the path to the backup catalog.

```sql
<using_catalog> ::= USING CATALOG BACKINT
| USING CATALOG PATH ( <path> )
```

In the file system, SAP HANA searches the specified locations for the backup catalog in the following order:

| **Path Specified...** | **Where Searched...** |
| --- | --- |
| 1.<br>In the SQL statement (optional):<br> `USING CATALOG PATH` | The path specified is searched for a backup catalog.<br>No subdirectories are searched. |
| 2.<br>Configured path. | The path to be searched is specified by the following parameter:<br> `basepath_catalogbackup`<br>This parameter is in the `persistence` section of the `global.ini` parameter file. |

#### limit_offset

The following options can be used with SAP HANA tenant databases:

- `LIMIT <limit>` restricts the number of elements returned. If `LIMIT <limit>` is not specified, then a default value of 10 is used.
- `OFFSET <offset>` defines the number of data backups to skip at the beginning of the list. If `OFFSET <offset>` is not specified, then no data backups are skipped.

```sql
<limit_offset> ::= LIMIT <int_const> [OFFSET <int_const>]
```

## Description

The most recent backup catalog available is searched at either the default log backup location or at the location specified by `<path_definition>`. You can restrict the search to only a third-party backup tool by using `USING CATALOG BACKINT`.

### BACKUP COMPLETE LIST DATA

The `COMPLETE` option provides a list of complete data backups that can be used for a recovery. For this reason, no `<until_definition>` is used with `BACKUP COMPLETE LIST DATA`. The `COMPLETE` option lists all the data backups from the backup catalog, starting with the most recent. This includes data backups that are not visible as a result of a previous recovery.

### Error Handling

The result set of `BACKUP LIST DATA` is written to an XML file named `strategyOutput.xml` in the SAP HANA trace directory.

If no result set is returned, `strategyOutput.xml` is still written, but is empty.

`BACKUP LIST DATA` only reports an error to the client if there is a syntax error, or if an incorrect system source definition was specified.

An SQL error is not always returned. If `strategyOutput.xml` was not created or was rewritten, check the `backup.log` for error messages.

For more information, see backup.log in the SAP HANA Administration Guide (SAP HANA Database Backup and Recovery).

## Permissions

Privilege needed:

`FOR <DATABASE>`: DATABASE RECOVERY OPERATOR or DATABASE ADMIN

## Related Information

backup.log (SAP HANA Administration Guide (SAP HANA Database Backup and Recovery))
