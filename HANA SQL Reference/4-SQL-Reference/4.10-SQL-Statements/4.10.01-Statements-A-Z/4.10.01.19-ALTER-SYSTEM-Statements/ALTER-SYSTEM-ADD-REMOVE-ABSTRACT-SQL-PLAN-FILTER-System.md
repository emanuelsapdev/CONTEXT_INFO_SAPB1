# 4.10.1.19.1 ALTER SYSTEM {ADD | REMOVE} ABSTRACT SQL PLAN FILTER (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 467–469

Starts or stops capturing abstract SQL plans for queries that match the specified filters.

## Syntax

```sql
ALTER SYSTEM ADD ABSTRACT SQL PLAN FILTER <filter_name>
   SET <predicate_list>
| ALTER SYSTEM REMOVE ABSTRACT SQL PLAN FILTER <target_filter>
```

## Syntax Element

#### filter_name

Specifies the name of the filter.

```sql
<filter_name>::= <string_literal>
```

##### SET predicate_list

Specifies the predicates that must be matched for the filter to be applied.

```sql
<predicate_list>::= <predicate>[, <predicate>...]
<predicate>::= '<key>' = '<value>'
<key>::= APPLICATION USER NAME
   | APPLICATION NAME
   | USER NAME
   | SCHEMA NAME
   | XS APPLICATION USER NAME
<value>::= <string_literal>
```

#### REMOVE

Removes the specified abstract SQL plan filter.

##### target_filter

Specifies the name of a specific filter to remove or that all filters should be removed.

```sql
<target_filter>::= <filter_name> | ALL
```

## Description

Abstract SQL plans are captured for queries that all of the specified predicates for a filter. If there are multiple filters defined, then a query is checked against all filters, and if the query matches any filter, the query is captured.

## Example

The following example defines a filter that captures abstract SQL plans for applications named App1.

```sql
ALTER SYSTEM ADD ABSTRACT SQL PLAN FILTER 'abc' SET 'APPLICATION NAME'='App1';
```

The following example defines a filter that captures abstract SQL plans for applications named App1 or with the application user name TEST.

```sql
ALTER SYSTEM ADD ABSTRACT SQL PLAN FILTER 'def' SET 'APPLICATION NAME'='App2',
'APPLICATION USER NAME'='TEST’;
```

The following example deletes the filter named abc.

```sql
ALTER SYSTEM REMOVE ABSTRACT SQL PLAN FILTER 'abc';
```

The following example deletes all filters that have been defined.

```sql
ALTER SYSTEM REMOVE ABSTRACT SQL PLAN FILTER ALL;
```

## Related Information

ALTER SYSTEM {ADD | REMOVE} ABSTRACT SQL PLAN FILTER (System Management) [→](ALTER-SYSTEM-ADD-REMOVE-ABSTRACT-SQL-PLAN-FILTER-System.md) ALTER SYSTEM {ENABLE | DISABLE | REMOVE} ABSTRACT SQL PLAN (System Management) [→](ALTER-SYSTEM-ENABLE-DISABLE-REMOVE-ABSTRACT-SQL-PLAN-System.md) ALTER SYSTEM MIGRATE ABSTRACT SQL PLAN (System Management) [→](ALTER-SYSTEM-MIGRATE-ABSTRACT-SQL-PLAN-System-Management.md) ALTER SYSTEM {START | STOP} APPLY ABSTRACT SQL PLAN (System Management) [→](ALTER-SYSTEM-START-STOP-APPLY-ABSTRACT-SQL-PLAN-System.md) ALTER SYSTEM UPDATE ABSTRACT SQL PLAN Statement (System Management) [→](ALTER-SYSTEM-UPDATE-ABSTRACT-SQL-PLAN-Statement-System.md) ABSTRACT_SQL_PLANS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/ABSTRACT_SQL_PLANS-System-View.md) M_ABSTRACT_SQL_PLAN_OVERVIEW System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_ABSTRACT_SQL_PLAN_OVERVIEW-System-View.md) M_ABSTRACT_SQL_PLAN_STATISTICS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_ABSTRACT_SQL_PLAN_STATISTICS-System-View.md)
