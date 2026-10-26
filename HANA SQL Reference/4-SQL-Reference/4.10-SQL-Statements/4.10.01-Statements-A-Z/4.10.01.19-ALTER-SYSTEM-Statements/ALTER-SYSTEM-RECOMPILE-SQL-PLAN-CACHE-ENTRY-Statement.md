# 4.10.1.19.43 ALTER SYSTEM RECOMPILE SQL PLAN CACHE ENTRY Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 532–533

Invalidates the designated plan cache entry so that it is recompiled during the next execution time.

## Syntax

```sql
ALTER SYSTEM RECOMPILE SQL PLAN CACHE ENTRY <plan_id>
```

## Syntax Elements

#### plan_id

Specifies the entry you want to recompile.

```sql
<plan_id> ::= <integer_literal>
```

Obtain the `<plan_id>` from the PLAN_ID column of the M_SQL_PLAN_CACHE monitoring view.

## Description

When invalidated, the entry is recompiled during the next execution time. Use this command when significant changes have occurred to the data cardinalities acted upon by the query plan.

## Permissions

You must have the OPTIMIZER ADMIN privilege to execute this statement.

## Example

Flag the plan cache entry with plan_id 247 for recompilation.

```sql
ALTER SYSTEM RECOMPILE SQL PLAN CACHE ENTRY 247;
```

## Related Information

[M_SQL_PLAN_CACHE System View](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SQL_PLAN_CACHE-System-View.md)
