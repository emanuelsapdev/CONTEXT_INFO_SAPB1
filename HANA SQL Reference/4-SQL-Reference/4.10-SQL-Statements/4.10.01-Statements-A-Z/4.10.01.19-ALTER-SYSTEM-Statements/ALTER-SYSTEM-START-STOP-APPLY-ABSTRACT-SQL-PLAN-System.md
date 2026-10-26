# 4.10.1.19.56 ALTER SYSTEM {START | STOP} APPLY ABSTRACT SQL PLAN (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 550–551

Starts or stops matching executed queries with captured abstract SQL plans.

## Syntax

```sql
ALTER SYSTEM { START | STOP } APPLY ABSTRACT SQL PLAN
```

## Syntax Elements

#### START

Loads all valid abstract SQL plans from the ABSTRACT_SQL_PLANS system table into the plan stability manager.

Wherever possible, any newly compiled SELECT statements are based on the abstract SQL plans. Queries are checked against the stored abstract plans and the abstract plan is used to generate an exection plan. When the plan is invalidated during generating an execution plan due to an error, the reason for the invalidation will be stored in the NOTES column in ABSTRACT_SQL_PLANS.

#### STOP

Stops the query optimizer from checking queries against stored abstract plans. STOP also unloads all valid abstract SQL plans in the ABSTRACT_SQL_PLANS system table from the plan cache; the optimizer stops using abstract SQL plans to execute queries.

## Description

Starts or stops matching executed queries with captured abstract SQL plans.

**Plan cache eviction policy:** When this statement is executed, any stored plans with the status **enabled** are evicted.

## Related Information

ALTER SYSTEM {ADD | REMOVE} ABSTRACT SQL PLAN FILTER (System Management) [→](ALTER-SYSTEM-ADD-REMOVE-ABSTRACT-SQL-PLAN-FILTER-System.md) ALTER SYSTEM {ENABLE | DISABLE | REMOVE} ABSTRACT SQL PLAN (System Management) [→](ALTER-SYSTEM-ENABLE-DISABLE-REMOVE-ABSTRACT-SQL-PLAN-System.md) ALTER SYSTEM MIGRATE ABSTRACT SQL PLAN (System Management) [→](ALTER-SYSTEM-MIGRATE-ABSTRACT-SQL-PLAN-System-Management.md) ALTER SYSTEM {START | STOP} CAPTURE ABSTRACT SQL PLAN (System Management) [→](ALTER-SYSTEM-START-STOP-CAPTURE-ABSTRACT-SQL-PLAN-System.md) ALTER SYSTEM UPDATE ABSTRACT SQL PLAN Statement (System Management) [→](ALTER-SYSTEM-UPDATE-ABSTRACT-SQL-PLAN-Statement-System.md) ABSTRACT_SQL_PLANS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/ABSTRACT_SQL_PLANS-System-View.md) M_ABSTRACT_SQL_PLAN_OVERVIEW System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_ABSTRACT_SQL_PLAN_OVERVIEW-System-View.md) M_ABSTRACT_SQL_PLAN_STATISTICS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_ABSTRACT_SQL_PLAN_STATISTICS-System-View.md)
