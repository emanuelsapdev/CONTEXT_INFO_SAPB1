# 4.10.1.19.50 ALTER SYSTEM RESET MONITORING VIEW Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 540–541

Resets statistics data for the specified monitoring view.

## Syntax

```sql
ALTER SYSTEM RESET MONITORING VIEW <view_name>
```

## Syntax Elements

#### view_name

Specifies the name of the resettable monitoring view to be reset.

```sql
<view_name> ::= [<schema_name>.]<identifier>

<schema_name> ::= <unicode_name>
```

Not all monitoring views can be reset using this command. The names of views that can be reset have the suffix _RESET.

## Description

Use this command to define a starting point for your measurements. First, you reset the monitoring view, and then you execute an action. After the action is completed, query the _RESET version of the monitor view to get the statistical information gathered since the last reset.

## Example

Reset the "SYS"."M_HEAP_MEMORY_RESET" monitoring view.

```sql
ALTER SYSTEM RESET MONITORING VIEW "SYS"."M_HEAP_MEMORY_RESET";
```
