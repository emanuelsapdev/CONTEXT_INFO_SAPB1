# 4.10.1.19.63 ALTER SYSTEM UPDATE ABSTRACT SQL PLAN Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 561–562

Updates the location information for abstract SQL plans.

## Syntax

```sql
ALTER SYSTEM UPDATE ABSTRACT SQL PLAN
   SET LOCATION <location_info_map_list> ALL
```

## Syntax Element

#### SET LOCATION location_info_map_list

Specifies the location of the abstract SQL plan. When you specify the location, then the location information of the target abstract SQL plan is updated with the specified location information map and then imported into the system.

```sql
<location_info_map_list> ::=
   <from_location> TO <to_location>[, <location_info_map_list> … ]
<from_location> ::= '<host_name>:<port_number>'
<to_location> ::= '<host_name>:<port_number>'
```

**ALL** Updates the location information for all abstract SQL plans.

## Description

Updates the location information for abstract SQL plans.

## Examples

The following statement updates the location of all abstract SQL plans:

```sql
ALTER SYSTEM UPDATE ABSTRACT SQL PLAN
   SET LOCATION 'selibm57:30103' TO 'selibm58:30103' ALL;
```

## Related Information

ALTER SYSTEM {ADD | REMOVE} ABSTRACT SQL PLAN FILTER (System Management) [→](ALTER-SYSTEM-ADD-REMOVE-ABSTRACT-SQL-PLAN-FILTER-System.md) ALTER SYSTEM {ENABLE | DISABLE | REMOVE} ABSTRACT SQL PLAN (System Management) [→](ALTER-SYSTEM-ENABLE-DISABLE-REMOVE-ABSTRACT-SQL-PLAN-System.md) ALTER SYSTEM MIGRATE ABSTRACT SQL PLAN (System Management) [→](ALTER-SYSTEM-MIGRATE-ABSTRACT-SQL-PLAN-System-Management.md) ALTER SYSTEM {START | STOP} CAPTURE ABSTRACT SQL PLAN (System Management) [→](ALTER-SYSTEM-START-STOP-CAPTURE-ABSTRACT-SQL-PLAN-System.md) ALTER SYSTEM {START | STOP} APPLY ABSTRACT SQL PLAN (System Management) [→](ALTER-SYSTEM-START-STOP-APPLY-ABSTRACT-SQL-PLAN-System.md) ABSTRACT_SQL_PLANS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/ABSTRACT_SQL_PLANS-System-View.md) M_ABSTRACT_SQL_PLAN_OVERVIEW System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_ABSTRACT_SQL_PLAN_OVERVIEW-System-View.md) M_ABSTRACT_SQL_PLAN_STATISTICS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_ABSTRACT_SQL_PLAN_STATISTICS-System-View.md)
