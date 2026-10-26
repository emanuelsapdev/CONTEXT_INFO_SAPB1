# 4.10.1.19.61 ALTER SYSTEM STOP DATABASE Statement (Tenant Database Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 558–560

Stops the specified database.

## Syntax

```sql
ALTER SYSTEM STOP DATABASE <database_name> [ IMMEDIATE [ WITH COREFILE ] ]
```

## Syntax Elements

#### database_name

Specifies the name of database to stop.

```sql
<database_name> ::= <identifier>
```

#### IMMEDIATE

Immediately stops the database without waiting for a regular shutdown.

#### WITH COREFILE

Writes a core dump file.

## Description

Executing this statement stops all of the services that belong to the database on all hosts The database is stopped immediately even if users are connected. Open transactions are aborted and rolled back; no save point operation is forced. It is not possible to back up a stopped database. This statement can only be issued from the SYSTEM database (systemDB) and is only available for SAP HANA tenant databases.

## Permissions

You must have the DATABASE ADMIN or DATABASE STOP privilege to use this statement.

## Example

Stop the database named my_database.

```sql
ALTER SYSTEM STOP DATABASE my_database;
```
