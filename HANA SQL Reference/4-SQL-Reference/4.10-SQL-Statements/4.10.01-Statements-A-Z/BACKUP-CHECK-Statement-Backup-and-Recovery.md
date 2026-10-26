# 4.10.1.31 BACKUP CHECK Statement (Backup and Recovery)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 659–661

Checks that required disk space for a backup is available in a specified location.

## Syntax

```sql
BACKUP CHECK [FOR <database_name>] <data_file_definition> SIZE <size>
```

## Syntax Elements

#### database_name

Specifies the database to be checked.

```sql
<database_name> ::= <identifier>
```

The database name can only be specified for an SAP HANA multitenant system.

#### data_file_definition

Specifies the location in the file system to be checked for sufficient space.

```sql
<data_file_definition> ::= USING FILE ( <file_name_prefix> )
<file_name_prefix> ::= <string_const>
```

#### size

Specifies the amount of memory in bytes that is required for the backup.

```sql
<size> ::= <integer>
```

## Description

If insufficient space is available or the folder does not exist, then an error message is returned.

Requirements:

- Executed on the system database only
- The system database must be online
- If a `<database_name>` is specified, then the specified database must be online as well

## Permissions

Privileges needed:

BACKUP OPERATOR or BACKUP ADMIN

`FOR <database_name>`: DATABASE BACKUP OPERATOR, DATABASE BACKUP ADMIN, or DATABASE ADMIN

## Example

Check whether 50GB of space are available in the `/backup/data` folder:

```sql
BACKUP CHECK USING FILE ('/backup/data') SIZE 53687091200;
```
