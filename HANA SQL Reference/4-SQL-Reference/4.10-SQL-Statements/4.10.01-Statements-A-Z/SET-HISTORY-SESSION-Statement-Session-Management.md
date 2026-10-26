# 4.10.1.145 SET HISTORY SESSION Statement (Session Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1094–1097

Allows the current database session to view a previous version of history tables.

## Syntax

```sql
SET HISTORY SESSION TO <when>
```

## Elements

#### when

Specifies the time period of the history table that should be used in the current database session.

```sql
<when> ::=
 NOW
 | COMMIT ID <commit_id>
 | UTCTIMESTAMP <timestamp>
```

##### NOW

Specifies that the database session uses the current version of the history table.

##### COMMIT ID commit_id

Specifies that the database session uses a version of the database table that was available at a specific commit ID.

```sql
COMMIT ID <commit_id>
 <commit_id> ::= <unsigned_integer>
```

##### UTCTIMESTAMP timestamp

Specifies that the database session uses a version of the database table that was available at a specific timestamp.

```sql
<timestamp> ::= <string_literal>
```

The timestamp must be in the format 'YYYY-MM-DD HH:MM:SS[.FF7]'.

## Description

Specify the required table version by COMMIT ID or UTCTIMESTAMP format. You can also set the session to see the current state of history tables by using the NOW parameter.

This command only affects history tables; normal tables remain unchanged. This command cannot be executed in autocommit on mode or nologflush mode.

As an alternative to using SET HISTORY SESSION, you can also use statement-level time travel.

## Examples

Create a history column on table x so you can view the table's history.

```sql
CREATE HISTORY COLUMN TABLE x ( a int, b int ); // after turning off auto commit
```

Insert values into table x.

```sql
INSERT INTO x VALUES (1,1);
 COMMIT;
 INSERT INTO x VALUES (2,2);
 COMMIT;
```

Obtain the commit ID of the last commit.

```sql
SELECT last_commit_id
FROM M_HISTORY_INDEX_LAST_COMMIT_ID
WHERE session_id = current_connection;
```

Before deleting the data, view the history of table x and perform a select.

View the history of table x using a timestamp and perform a select. Replace `<last_commit_id>` with the value you obtained from the previous query.

```sql
SET HISTORY SESSION TO COMMIT ID <last_commit_id>;
 SELECT * FROM x;
```

Delete all the data from table x.

```sql
SET HISTORY SESSION TO NOW;
DELETE FROM x;
COMMIT;
```

The select query above returns the two records (1,1) and (2,2), which existed before you deleted the contents of table x.

Obtain the `<last_commit_id>` timestamp.

```sql
SELECT COMMIT_TIME FROM SYS.TRANSACTION_HISTORY WHERE commit_id =
<last_commit_id>;
```

View the history of table x using a timestamp and perform a select. Replace `<commit_time>` with the value you obtained from the previous query.

```sql
SET HISTORY SESSION TO UTCTIMESTAMP '<commit_time>';
 SELECT * FROM x;
```

The select query above returns the two records (1,1) and (2,2), which existed before you deleted the contents of table x.

Set the history session to the current commit state and perform a select.

```sql
SET HISTORY SESSION TO NOW;
 SELECT * FROM x;
```

The select query returns an empty table because, at the current state, the table has had all of its data deleted.

## Related Information

Data Types [→](../../4.03-Data-Types/README.md) M_HISTORY_INDEX_LAST_COMMIT_ID System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_HISTORY_INDEX_LAST_COMMIT_ID-System-View.md) TRANSACTION_HISTORY System View [→](../../../6-System-Views-Reference/6.01-System-Views/TRANSACTION_HISTORY-System-View.md) HISTORY COLUMN Option (Time Travel) [→](4.10.01.68-CREATE-TABLE/4.10.01.68.03-HISTORY-COLUMN-Option-Time-Travel.md)
