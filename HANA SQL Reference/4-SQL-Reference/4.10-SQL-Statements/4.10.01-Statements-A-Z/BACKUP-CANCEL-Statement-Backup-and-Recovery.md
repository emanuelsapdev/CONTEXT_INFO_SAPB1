# 4.10.1.29 BACKUP CANCEL Statement (Backup and Recovery)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 655–657

Cancels a running data backup.

## Syntax

```sql
BACKUP CANCEL [FOR <database_name>] <backup_ID>
```

## Syntax Elements

#### database_name

Specifies the name of an SAP HANA database.

```sql
<database_name> ::= <identifier>
```

#### backup_ID

Specifies the backup to be canceled.

```sql
<backup_ID> ::= <integer>
```

## Description

Requirements:

- Executed on the system database only
- The system and the tenant database(s) must be online
1. Find the backup ID. When a data backup is started, the system assigns a unique ID to the data backup. To find the backup ID of the running data backup, use the monitoring view M_BACKUP_CATALOG, which provides an overview of information about backup and recovery activities. Use the following SQL statement to display the backup ID:

```sql
SELECT BACKUP_ID FROM "M_BACKUP_CATALOG"
   WHERE ENTRY_TYPE_NAME = 'complete data backup'
   AND STATE_NAME = 'running'
   ORDER BY SYS_START_TIME DESC;
```

2. To cancel the running data backup, use the following SQL statement:

```sql
BACKUP CANCEL <backup_ID>
```

The data backup is canceled asynchronously.

3. Check that the data backup was canceled. Use the monitoring view M_BACKUP_CATALOG to display the status of the canceled data backup. The status canceled confirms that the backup was canceled successfully. When the backup status is canceled, you can start a new data backup.

If you cancel a running data backup that is waiting for other resources, the cancelation is postponed until the cause of the wait situation has been resolved. Until that time, the backup is flagged as cancel pending.

## Permissions

Privileges needed:

BACKUP OPERATOR or BACKUP ADMIN

`FOR <database_name>`: DATABASE BACKUP OPERATOR, DATABASE BACKUP ADMIN, or DATABASE ADMIN

## Example

Cancel the data backup with ID `1331715084250`:

```sql
BACKUP CANCEL 1331715084250;
```
