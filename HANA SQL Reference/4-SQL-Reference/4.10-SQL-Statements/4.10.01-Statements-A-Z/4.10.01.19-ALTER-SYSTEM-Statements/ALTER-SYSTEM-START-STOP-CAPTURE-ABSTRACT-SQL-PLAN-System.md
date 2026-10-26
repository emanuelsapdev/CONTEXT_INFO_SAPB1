# 4.10.1.19.57 ALTER SYSTEM {START | STOP} CAPTURE ABSTRACT SQL PLAN (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 551–553

Starts or stops capturing abstract SQL plans for queries that are executed against the database.

## Syntax

```sql
ALTER SYSTEM START CAPTURE ABSTRACT SQL PLAN
    [ FOR USER <user_name_list> ]
    [ WITH SQL PLAN CACHE ]
| ALTER SYSTEM STOP CAPTURE ABSTRACT SQL PLAN
```

## Syntax Element

#### START

Starts the collection of abstract SQL plans for newly compiled queries.

##### FOR USER user_name_list

Captures and stores abstract SQL plans for newly compiled queries that are executed by the specified users.

```sql
<user_name_list>::= <user_name>[, <user_name>]...
```

##### WITH SQL PLAN CACHE

Controls whether cached SQL queries in the SQL plan cache are captured. Specify this clause to capture newly compiled SQL queries and capture cached SQL queries. Otherwise, only newly compiled SQL queries are captured (the default).

This clause recompiles the queries that are currently cached in the system.

#### STOP

Stops the collection of abstract SQL plans for newly compiled queries.

If a background job is still capturing plans when this statement is executed, then plan stability does not capture any more plans. The stop capture takes effect after the current statement that is being captured is finished.

## Description

The capture process runs in the background while selected queries are executed.

## Example

Start capturing abstract SQL plans for all database users:

```sql
ALTER SYSTEM START CAPTURE ABSTRACT SQL PLAN;
```

Capture abstract SQL plans only for the specified users:

```sql
ALTER SYSTEM START CAPTURE ABSTRACT SQL PLAN FOR USER TESTUSER1, TESTUSER2;
```

## Related Information

ALTER SYSTEM {ENABLE | DISABLE | REMOVE} ABSTRACT SQL PLAN (System Management) [→](ALTER-SYSTEM-ENABLE-DISABLE-REMOVE-ABSTRACT-SQL-PLAN-System.md) ALTER SYSTEM MIGRATE ABSTRACT SQL PLAN (System Management) [→](ALTER-SYSTEM-MIGRATE-ABSTRACT-SQL-PLAN-System-Management.md) ALTER SYSTEM {START | STOP} APPLY ABSTRACT SQL PLAN (System Management) [→](ALTER-SYSTEM-START-STOP-APPLY-ABSTRACT-SQL-PLAN-System.md) ALTER SYSTEM UPDATE ABSTRACT SQL PLAN Statement (System Management) [→](ALTER-SYSTEM-UPDATE-ABSTRACT-SQL-PLAN-Statement-System.md) ABSTRACT_SQL_PLANS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/ABSTRACT_SQL_PLANS-System-View.md) M_ABSTRACT_SQL_PLAN_OVERVIEW System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_ABSTRACT_SQL_PLAN_OVERVIEW-System-View.md) M_ABSTRACT_SQL_PLAN_STATISTICS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_ABSTRACT_SQL_PLAN_STATISTICS-System-View.md)
