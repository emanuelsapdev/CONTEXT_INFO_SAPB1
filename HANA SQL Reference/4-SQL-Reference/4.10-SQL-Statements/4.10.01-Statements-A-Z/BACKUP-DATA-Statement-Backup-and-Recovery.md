# 4.10.1.33 BACKUP DATA Statement (Backup and Recovery)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 663–668

Creates a data backup of the specified database in the specified location.

## Syntax

```sql
BACKUP DATA [<backup_delta>] [FOR <database_name>]
   <data_backup_definition> [<additional_option_list>] [<comment>]
```

## Syntax Elements

#### backup_delta

Specifies the type of backup to be created.

```sql
<backup_delta> ::= INCREMENTAL | DIFFERENTIAL
```

If this parameter is omitted, a complete backup is created.

#### database_name

If you are connected to the system database, specifies the name of the tenant database to back up.

```sql
<database_name> ::= <identifier>
```

#### data_backup_definition

Defines the file location where the backup is created.

```sql
<data_backup_definition> ::=
 USING { <data_backup_definition_file> | <data_backup_definition_backint>
[DISABLE ES ENCRYPTION CHANGE]}
<data_backup_definition_file> ::=
 FILE ( '<prefix>' | '<path>', '<prefix>' )
<data_backup_definition_backint> ::=
 BACKINT ( '<prefix>' | '<path>', '<prefix>' )
```

You can provide the path and prefix either as a single string or as two separate strings for path and prefix. The trailing path delimiter in `<path>` may be omitted.

#### DISABLE ES ENCRYPTION CHANGE

Applies to SAP HANA dynamic tiering only.

When you specify the DISABLE ES ENCRYPTION CHANGE clause, extended storage copies blocks from the database to the backup archive without modifying their encryption state. This can improve backup and recovery speeds for extended storage.

Changes to the encryption state during recovery are not permitted with speeds for extended storage.

SAP recommends you do not specify DISABLE ES ENCRYPTION CHANGE when data volume encryption is enabled.

> **Note**
>
> If backup encryption is enabled, specifying DISABLE ES ENCRYPTION CHANGE results in an error.

You can monitor the DISABLE ES ENCRYPTION CHANGE allowed or disallowed status in the M_BACKUP_CATALOG system view.

#### additional_option_list

Additional options for backup.

```sql
<additional_option_list> ::= <additional_option> [...]
```

```sql
<additional_option> ::= ASYNCHRONOUS | TOOLOPTION '<parameter_string>'
```

With ASYNCHRONOUS, the system does not wait for the backup process to end. The status of the backup is visible in the M_BACKUP_CATALOG system view. By default, a synchronous backup is created.

TOOLOPTION is only available for BACKINT.

TOOLOPTION passes a vendorspecific parameter string to a third-party backup tool. The string has a maximum length of 4096 bytes.

#### comment

Specifies a descriptive comment for the backup.

```sql
<comment> ::= COMMENT '<string_const>'
```

## Description

Creates a data backup of the specified database in the specified location.

> **Note**
>
> If a data backup with the same name already exists in the specified location, it will be overwritten by the newest data backup.

To set up data backup in batch mode, set up a batch user and authorize this user to create backups.

For batch processing with SAP HANA HDBSQL, use the SAP HANA secure user store (hdbuserstore). Otherwise, the password used to connect to the database is visible in the process list. hdbuserstore is installed as part of the client package.

For data backups for dynamic tiering extended storage, the global system property `es_data_backup_buffer_size` is a tuning option that may optimize backup performance.

## Permissions

Privileges needed:

BACKUP OPERATOR or BACKUP ADMIN

`FOR <database_name>`: DATABASE BACKUP OPERATOR, DATABASE BACKUP ADMIN, or DATABASE ADMIN

## Examples

1. Create a data backup of the entire database. This creates a data backup file of every relevant service in the default backup destination. Label the backup 'data backup of 2018-10-16' by using the COMMENT clause.

```sql
BACKUP DATA USING FILE ('COMPLETE') COMMENT 'data backup of 2018-10-16';
```

The data backup files are prepended with the prefix COMPLETE. The comment string is recorded in the backup catalog and is visible in the M_BACKUP_CATALOG system view. The following files are created in the default data backup directory:

- COMPLETE_databackup_0_1
- COMPLETE_databackup_1_1
- COMPLETE_databackup_2_1
2. Create a data backup of the entire database and create a data backup for every relevant service in the default backup destination.

```sql
BACKUP DATA USING FILE ('COMPLETE');
```

The data backup files are prepended with the prefix COMPLETE. The following files are created in the default data backup directory:

- COMPLETE_databackup_0_1
- COMPLETE_databackup_1_1
- COMPLETE_databackup_2_1
3. Create a data backup of the entire database and create a data backup for every relevant service in the directory `/backup` and the prefix `MONDAY`.

```sql
BACKUP DATA USING FILE ('/backup/MONDAY');
```

Create the same file using alternative syntax with separate strings to specify path and prefix.

```sql
BACKUP DATA USING FILE ('/backup/', 'MONDAY');
```

Create the same file using alternative syntax with separate strings to specify path and prefix, omitting the last path delimiter.

```sql
BACKUP DATA USING FILE ('/backup', 'MONDAY');
```

Data backup files are prepended with the string MONDAY. The following files are created:

```sql
/backup/MONDAY_databackup_0_1/backup/MONDAY_databackup_1_1/backup/
MONDAY_databackup_2_1;
```

4. Create a data backup of the entire database. This creates a data backup file for every relevant service in the directory `/backup`.

```sql
BACKUP DATA USING FILE ('/backup/') ASYNCHRONOUS;
```

Data backups are not labeled. The ASYNCHRONOUS option returns to the client immediately after starting the backup operation, even though the data backup is still running. The following backups are created:

- /backup/databackup_0_1
- /backup/databackup_1_1
- /backup/databackup_2_1
5. Create a data backup of the entire instance. This creates a data backup for each service using the third-party backup tool.

```sql
BACKUP DATA USING BACKINT ('MyBackIntBackup') TOOLOPTION 'This is my tool
option';
```

Data backups are prepended with the prefix `MyBackIntBackup`. The TOOLOPTION string `'This is my tool option'` is forwarded to the third-party backup tool. The following backups are created in the third-party backup tool:

```sql
MyBackIntBackup_databackup_0_1 MyBackIntBackup_databackup_1_1
MyBackIntBackup_databackup_2_1;
```

6. Create an incremental backup in the default data backup directory. Use the prefix `2018-10-16`.

```sql
BACKUP DATA INCREMENTAL USING FILE ('2018-10-16');
```

The example SQL statement would create backups with the following names (all on one line):

```sql
2018-10-16_databackup_incremental_1426237023821_1426237028496_0_1 2018-10-16_
databackup_incremental_1426237023821_1426237028496_1_1
2018-10-16_databackup_incremental_
1426237023821_1426237028496_2_1
2018-10-16_databackup_incremental_1426237023821_1426237028496_3_1;
```

7. Create a differential backup based on the last data backup.

```sql
BACKUP DATA DIFFERENTIAL USING FILE ('2018-10-16');
```

The example SQL statement would create backups with the following names (all on one line):

```sql
2018-10-16_databackup_differential_1426237023821_1426237780534_0_1
2018-10-16_databackup_differential_
1426237023821_1426237780534_1_1
2018-10-16_databackup_differential_1426237023821_1426237780534_2_1 2018-10-16_
databackup_differential_1426237023821_1426237780534_3_1;
```

8. (SAP HANA dynamic tiering only.) Create a data backup of the entire database. Extended storage copies blocks from the database to the backup archive without modifying their encryption state.

```sql
BACKUP DATA USING FILE ('my_backup') DISABLE ES ENCRYPTION CHANGE;
```

Changes to the encryption state during recovery are not permitted with these backups. SAP recommends you do not specify DISABLE ES ENCRYPTION CHANGE when data volume encryption is enabled.

## Related Information

M_BACKUP_CATALOG System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_BACKUP_CATALOG-System-View.md) Global System Properties (global.ini) in the SAP HANA Dynamic Tiering Administration Guide [→](../../../5-Additional-SAP-HANA-Contexts/5.02-Dynamic-Tiering/5.02.07-ALTER-SYSTEM-ALTER-CONFIGURATION-DT/5.02.07.02-Global-System-Properties-global-ini.md)
