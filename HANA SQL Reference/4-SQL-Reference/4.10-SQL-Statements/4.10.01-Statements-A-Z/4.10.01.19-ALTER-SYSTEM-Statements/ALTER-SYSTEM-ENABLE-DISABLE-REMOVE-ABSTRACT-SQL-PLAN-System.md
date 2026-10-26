# 4.10.1.19.4 ALTER SYSTEM {ENABLE | DISABLE | REMOVE} ABSTRACT SQL PLAN (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 472–474

Enables or disables execution plan generation for abstract SQL plans, or removes plans from the ABSTRACT_SQL_PLANS table.

## Syntax

```sql
ALTER SYSTEM <enable_disable_remove_action> ABSTRACT SQL PLAN ENTRY <target>
```

## Syntax Elements

#### enable_disable_remove_action

Specifies the action to perform.

```sql
<enable_disable_remove_action> ::= { ENABLE | DISABLE | REMOVE }
```

##### ENABLE

Enables the abstract SQL plans for use by the optimizer.

##### DISABLE

Disables the abstract SQL plans for use by the optimizer.

##### REMOVE

Permanently deletes the abstract SQL plans.

#### target

Specifies the scope of `<action>`.

```sql
<target> ::= ALL | FOR <id_list>
<id_list> ::= <plan_id> [, <plan_id> [,...] ]
```

**id_list** Specifies the plans to which the action applies.

`<id_list>` applies the `<action>` as follows:

| **Action** | **Behavior** |
| --- | --- |
| ENABLE | Enable the abstract SQL plan entries specified in the `<id_list>`. If multiple abstract SQL plan entries of the same query are specified in the `<id_list>`, then the last entry of the same query in the list is enabled. |
| DISABLE | Disable the abstract SQL plan entries specified in the `<id_list>`. |
| REMOVE | Remove the abstract SQL plan entries specified in the `<id_list>`. |

##### ALL

ALL applies the action to all abstract SQL plans.

ALL applies the `<action>` to all abstract SQL plans, as follows:

| **Action** | **Behavior** |
| --- | --- |
| ENABLE | For each abstract SQL plan query that does not have any enabled entry, enable the first captured entry. |
| DISABLE | Disable all enabled abstract SQL plan entries. |
| REMOVE | Remove all abstract SQL plan entries. |

## Description

This statement controls optimizer access to abstract SQL plans.

**Plan cache eviction policy:** When an ENABLE or DISABLE ABSTRACT SQL PLAN ENTRY ALL statement is executed, any captured plans implicated by`<target>` are evicted. When a REMOVE ABSTRACT SQL PLAN ENTRY ALL statement is executed, any captured plans implicated by `<target>` with status **enabled** are evicted.

## Example

The following example removes all abstract SQL plans:

```sql
ALTER SYSTEM REMOVE ABSTRACT SQL PLAN ENTRY ALL;
```

The following example enables the single abstract SQL plan with ID 9630002 for use by the optimizer:

```sql
ALTER SYSTEM ENABLE ABSTRACT SQL PLAN ENTRY FOR 9630002;
```

## Related Information

ALTER SYSTEM {ADD | REMOVE} ABSTRACT SQL PLAN FILTER (System Management) [→](ALTER-SYSTEM-ADD-REMOVE-ABSTRACT-SQL-PLAN-FILTER-System.md) ALTER SYSTEM MIGRATE ABSTRACT SQL PLAN (System Management) [→](ALTER-SYSTEM-MIGRATE-ABSTRACT-SQL-PLAN-System-Management.md) ALTER SYSTEM {START | STOP} CAPTURE ABSTRACT SQL PLAN (System Management) [→](ALTER-SYSTEM-START-STOP-CAPTURE-ABSTRACT-SQL-PLAN-System.md) ALTER SYSTEM {START | STOP} APPLY ABSTRACT SQL PLAN (System Management) [→](ALTER-SYSTEM-START-STOP-APPLY-ABSTRACT-SQL-PLAN-System.md) ALTER SYSTEM UPDATE ABSTRACT SQL PLAN Statement (System Management) [→](ALTER-SYSTEM-UPDATE-ABSTRACT-SQL-PLAN-Statement-System.md) ABSTRACT_SQL_PLANS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/ABSTRACT_SQL_PLANS-System-View.md) M_ABSTRACT_SQL_PLAN_OVERVIEW System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_ABSTRACT_SQL_PLAN_OVERVIEW-System-View.md) M_ABSTRACT_SQL_PLAN_STATISTICS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_ABSTRACT_SQL_PLAN_STATISTICS-System-View.md)
