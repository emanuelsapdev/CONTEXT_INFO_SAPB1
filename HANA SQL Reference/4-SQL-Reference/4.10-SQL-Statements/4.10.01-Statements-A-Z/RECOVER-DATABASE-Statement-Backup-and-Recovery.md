# 4.10.1.129 RECOVER DATABASE Statement (Backup and Recovery)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1004–1012

Recovers an SAP HANA database to a specific point in time or to a specific log position.

## Syntax

```sql
RECOVER DATABASE [ FOR <database_name> ]
  { <until_definition>
   [ <system_source_definition> ]
   [ <strategy_using_definition> ]
   [ <check_access_definition> ]
 [ <ignore_option_list> ]
}
```

## Syntax Elements

#### database_name

This option is only available for SAP HANA tenant databases.

Recovers a tenant database to a specific point in time.

```sql
<database_name> ::= <identifier>
```

After the recovery, the log is replayed and the tenant database is in an ACTIVE state.

#### until_definition

Defines the target of the recovery.

```sql
<until_definition> ::=
 UNTIL LOG POSITION <log_pos> AT VOLUME <volume_id>
[ <recover_additional_option_list> ]
 | UNTIL TIMESTAMP '<timestamp>' [ <recover_additional_option_list> ]
```

`<timestamp>` is interpreted as UTC time. For example, 3:00 p.m. means 3:00 p.m. UTC, not 3:00 p.m. in your local time zone.

##### recover_additional_option_list

Specifies additional recovery options.

```sql
<recover_additional_option_list> ::=
 <recover_additional_option>
 | <recover_additional_option> <recover_additional_option>
<recover_additional_option> ::= CLEAR LOG | SET LICENSE <string_const>
```

`CLEAR LOG` initializes the log area. The content of the log area is permanently lost. No log entries from the log area are used for the recovery.

If they are needed, the log entries from the log backups are replayed.

You must specify `CLEAR LOG` in the following situations:

- The log area is unusable.
- You are recovering the database to a different system.

`SET LICENSE` allows you to specify a license key during the recovery.

#### system_source_definition

Identifies the source system.

This option can only be used if a data backup from a third-party backup tool is used for the recovery.

```sql
<system_source_definition> ::= USING SOURCE '<system_id>'
```

`USING SOURCE` specifies that the data backup is of a database with a different SID or name than the target system.

To recover a tenant database using a Backint-based backup that was created in a system identified by the system ID PR1 and the name `TENANT_1`, the option would be:

```sql
<system_source_definition> ::= USING SOURCE 'TENANT_1@PR1'
```

To recover a Backint-based data backup from a single container system identified by the system ID PR1, use the following option:

```sql
USING SOURCE 'PR1'
```

#### strategy_using_definition

Specifies the location to search for the backup catalog, the data backup, and the log backups.

```sql
<strategy_using_definition> ::=
 <path_definition> [ <start_from_definition> ]
```

```sql
<path_definition> ::=
 [ <catalog_path_definition> ]
 [ USING LOG PATH ( <path_list> ) ]
 [ USING DATA PATH ( <path_list> ) ]
```

`USING LOG PATH` specifies the location of the log backup in the file system.

`USING DATA PATH` specifies the location of the data backup in the file system.

In the file system, SAP HANA searches the specified locations for backups in the following order:

| **Path Specified...** | **Where Searched...** |
| --- | --- |
| 1.<br>In the SQL statement (optional):<br> `USING LOG PATH <path list> USING DATA PATH <path list>` | The specified paths are searched for data backups or log backups.<br>All subdirectories are searched.<br>If a specified path is **relative**, the path is based on the backup paths specified by the following parameters:<br> `basepath_databackup basepath_logbackup`<br>These parameters are in the `persistence` section of the `global.ini` parameter file. |
| 2.<br>Configured paths. | The paths to be searched are specified by the following parameters:<br> `basepath_databackup basepath_logbackup`<br>These parameters are in the `persistence` section of the `global.ini` parameter file. |
| 3.<br>If no backups are found in the paths for 1. or 2. | The paths specified in the original backup catalog are searched for the backups. |

```sql
<catalog_path_definition> ::=
 USING CATALOG BACKINT | USING CATALOG PATH ( '<path>' )
```

To use a backup catalog that is in a third-party backup tool, use the option `USING CATALOG BACKINT`. When a backup catalog in a third-party backup tool is accessed, only the configured location is accessed. No traversal search for a backup catalog is done. You can specify a particular data backup using the `BACKUP_ID` option.

In the file system, SAP HANA searches the specified locations for the backup catalog in the following order:

| **Path Specified...** | **Where Searched...** |
| --- | --- |
| 1.<br>In the SQL statement (optional):<br> `USING CATALOG PATH` | The path specified is searched for a backup catalog.<br>No subdirectories are searched. |
| 2.<br>Configured path. | The path to be searched is specified by the following parameter:<br> `basepath_catalogbackup`<br>This parameter is in the `persistence` section of the `global.ini` parameter file. |

##### path_list

Defines the path to the backup.

```sql
<path_list> ::=
 '<path>'
 | <path_list>, '<path>'
```

##### start_from_and_guid_definition

```sql
<start_from_and_guid_definition> ::=
[<start_from_definition>] [<guid_definition>]
```

##### start_from_definition

```sql
<start_from_definition> ::=
 USING BACKUP_ID <int_const>
 | USING SNAPSHOT
 | USING RESUME
```

`USING BACKUP_ID` specifies the ID of the full data backup to use for recovery.

`USING SNAPSHOT` recovers the database from a data snapshot.

> **Note**
>
> You can recover SAP HANA using a data snapshot of an SAP HANA database with one or more tenant databases. When you recover SAP HANA from a data snapshot, you need to recover **both** the system database and then each tenant database separately. The tenant databases cannot be recovered together in one single operation.

`USING RESUME` continues a canceled or aborted recovery, without repeating the whole recovery from the start.

A resumed recovery must use the **same backup catalog** as the recovery that was canceled or aborted. To specify the backup catalog, use the following option:

- File-based backups: `USING CATALOG PATH ('<path>')`
- Third-party backup tools: `USING CATALOG BACKINT`

##### guid_definition

Defines the starting point of the backup using the global unique ID (GUID) of a log history.

If `RECOVER DATA` was already executed, you may need to use a different log history than the one proposed by default. To use a specific log history, use USING GUID. You can find a GUID for a specific log history in the `backup.log`.

```sql
<guid_definition> ::= USING GUID_ID '<guid>'
```

#### check_access_definition

Checks whether the backups are available in accordance with the recovery strategy.

`CHECK ACCESS` checks whether the required backups are available before the recovery is started. If one or more backups are not available, you are notified of this before the recovery starts, and the recovery is canceled before any changes are made to the database. If you do not check the availability of the required backups before recovery starts, missing backups will only be detected during the recovery. In this situation, you may need to restart or resume the recovery.

```sql
<check_access_definition> ::=
 CHECK ACCESS ALL
 | CHECK ACCESS USING FILE
 | CHECK ACCESS USING BACKINT
```

`CHECK ACCESS USING FILE` checks for backups in the file system.

`CHECK ACCESS USING BACKINT` checks for backups created with a third-party backup tool.

`CHECK ALL` checks for backups in both the file system and the third-party backup tool.

#### ignore_option_list

```sql
<ignore_option_list> ::= <ignore_option> [...]
```

```sql
<ignore_option> ::= IGNORE DELTA DATA BACKUPS | IGNORE WORKERGROUPS | IGNORE
COMPATIBILITY CHECK
```

`IGNORE DELTA DATA BACKUPS` uses log backups, without using incremental and differential backups.

`IGNORE WORKERGROUPS`: By default, when you recover a database from an indexserver that has worker groups, the target system must have worker groups with the same names as in the source system. Otherwise the recovery fails. `IGNORE WORKERGROUPS` removes this restriction. If worker groups with matching names are found in the target system, those worker groups are used. If no worker groups with matching names are found, the worker groups of the backup service are changed to the default to match those of the target system.

`IGNORE COMPATIBILITY CHECK`: By default, the version of the backup is checked for compatibility with the SAP HANA revision. You have the option to recover SAP HANA without performing this check.

> **Caution**
>
> Disabling the compatibility check may have unforeseen consequences. Use this option only in exceptional situations.

For more information, see SAP Note 1948334 (SAP HANA Database Update Paths for SAP HANA Maintenance Revisions)

## Description

`RECOVER DATABASE` recovers an SAP HANA database to a specific point in time or to a specific log position.

To recover a database, it must be offline. However, you can still execute SQL statements on the online system database to recover an offline tenant database.

To recover the system database from the command line (without using SAP HANA cockpit), use the `recoverSys.py` tool. To recover a tenant database from the command line, use an SQL interface such as hdbsql.

For more information about backup and recovery, including information about using `recoverSys.py`, refer to the SAP HANA Administration Guide (SAP HANA Database Backup and Recovery)

## Permissions

Privilege needed:

`FOR <database_name>`: DATABASE RECOVERY OPERATOR or DATABASE ADMIN

## Examples

### Scenario 1: Recovery to a Point in Time

The last complete data backup was created on Wednesday, October 21, 2020 at 8 a.m. CEST (6 a.m. UTC).

The database ran until 6pm CEST (4 p.m. UTC). You want to recover the database to its state at 5pm (3 p.m. UTC).

```sql
RECOVER DATABASE FOR TENANT_1 UNTIL TIMESTAMP '2020-10-21 15:00:00' CHECK ACCESS
ALL;
```

The database timestamp is interpreted as UTC time. 3 p.m. therefore means 3 p.m. UTC and not 3 p.m. CEST.Use the following statement to recover the tenant database named TENANT_1 to the specified point in time:

The specified timestamp is not included in the transactions to be redone. Only transactions with a commit timestamp before the target timestamp are redone.

### Scenario 2: Recovery to a Point in Time Using a Specific Directory

Recover the tenant database TENANT_1 to a point in time with a specific timestamp, by using a dedicated directory for data backups and further directories containing log backups.

Use the following statement:

```sql
RECOVER DATABASE FOR TENANT_1 UNTIL TIMESTAMP '2020-10-21 15:00:00' USING DATA
PATH ('/backup/WEDNESDAY/') USING LOG PATH ('/backup/logs1/','/backup/logs2/');
```

The backup catalog is taken from the configured default location, which could be a third-party backup tool or a directory in the file system.

For more information, see the SAP HANA Administration Guide (SAP HANA Database Backup and Recovery).

### Scenario 3: Recovery Using a Data Snapshot

Use a data snapshot to recover an SAP HANA with multiple tenant databases to its most recent state. Based on the restored data snapshot, log entries from the log area and log backups are applied.

You need to recover the system database and then each tenant database separately.

To recover the system database to its most recent state, use the following statement:

```sql
RECOVER DATABASE UNTIL TIMESTAMP '2020-10-21 15:00:00' USING SNAPSHOT;
```

To recover a tenant database to its most recent state using the data snapshot, use the following statement:

```sql
RECOVER DATABASE FOR TENANT_1 UNTIL TIMESTAMP '2027-10-21 15:00:00' USING
SNAPSHOT;
```

With USING SNAPSHOT, no paths are specified. Before the recovery is started, the data snapshot needs to be made available in the data area.

> **Note**
>
> To recover to the most recent state, the date needs to be later than the most recent state. In this example, we use the year 2027.

### Scenario 4: Recovery Using a Catalog Path

Use the following statement to recover the tenant database named TENANT_1 to theRecover the tenant database TENANT_1 to a point in time with a specific timestamp, using different locations in the file system for log backups and the backup catalog.

```sql
RECOVER DATABASE FOR TENANT_1 UNTIL TIMESTAMP '2020-10-21' USING CATALOG PATH ('/
hana/PR1/backup/catalog') USING LOG PATH ('/hana/HHB/backup/log') CHECK ACCESS
ALL;
```

### Scenario 5: Recover Using a Specific Log History

Recover the tenant database TENANT_1 to a specified log position in a log history specified by its persistence global unique ID (GUID).

```sql
RECOVER DATABASE FOR TENANT_1 UNTIL LOG POSITION 7553856 at volume 2 CLEAR LOG
USING GUID '41D53842-FA51-0017-3527-F4A470000005';
```

### Scenario 6: Resume a Recovery

Step 1: Recover SAP HANA database named PR1.

```sql
RECOVER DATABASE FOR PR1
                UNTIL TIMESTAMP '2020-10-21 05:00:00'
                CLEAR LOG
                USING CATALOG BACKINT
                USING LOG PATH ('/usr/sap/PR1/HDB/backup/log/DB_PR1')
                USING DATA PATH ('/usr/sap/PR1/SYS/global/hdb/backint/DB_PR1/')
                USING BACKUP_ID 1540499452637
                CHECK ACCESS USING FILE
```

Step 2: After the recovery is canceled, resume the recovery.

```sql
RECOVER DATABASE FOR PR1
                UNTIL TIMESTAMP '2020-10-21 05:00:00'
                CLEAR LOG
                USING CATALOG BACKINT
                USING RESUME
                CHECK ACCESS USING FILE
```

`USING CATALOG BACKINT` must be included in the SQL statement to resume recovery, as it was used in the recovery that was canceled. Note that in the resume statement, `USING LOG PATH` and `USING DATA PATH` are ignored.

### Scenario 7: Recover Using Backups in the File System and a Backup Catalog in a Third-Party Backup Tool

In this example, a tenant database `PR2` in SAP HANA system `PR2` is recovered using backups of tenant database `PR1` in SAP HANA system `PR1`. The backup catalog is in a third-party backup tool. The data backup was created in the file system of the source system, and was copied to the file system of the target system. `USING DATA PATH` is used to override the path specified in the source backup catalog with the file system directory that currently contains the data backup.

```sql
RECOVER DATABASE FOR PR2 UNTIL TIMESTAMP '2020' CLEAR LOG USING SOURCE 'PR1@PR1'
USING DATA PATH ('/hana/PR1/backup/data')
```

In this scenario, the log backups are in the third-party backup tool. If the log backups were in the file system, `USING LOG PATH` would be used to override the path specified in the source backup catalog with the file system directory that contains the log backup.

> **Note**
>
> To find out which backups are required to complete a recovery, you can use the `hdbbackupdiag` tool. You can also use `hdbbackupdiag` to check whether these backups are available and can be accessed.
>
> For more information, see Checking Whether a Recovery is Possible in the SAP HANA Administration Guide (SAP HANA Database Backup and Recovery).

### Scenario 8: Recover Using Backups in a Third-Party Backup Tool and a Backup Catalog in the File System

In this example, a tenant database `PR2` in SAP HANA system `PR2` is recovered using backups of tenant database `PR1` in SAP HANA system `PR1`. The backups are in the third-party backup tool. The backup catalog was created in the file system of the source system, and was copied to the file system of the target system. For this reason, `USING CATALOG PATH` is used to specify the location of the backup catalog to be used.

```sql
RECOVER DATABASE FOR PR2 UNTIL TIMESTAMP '2020' CLEAR LOG USING SOURCE 'PR1@PR1'
USING CATALOG PATH ('/hana/PR1/backup/catalog')
```

## Related Information

SAP Note 1948334 SAP Note 2050606 Change the Default Destination for File-Based Data Backups Change the Log Backup Destination
