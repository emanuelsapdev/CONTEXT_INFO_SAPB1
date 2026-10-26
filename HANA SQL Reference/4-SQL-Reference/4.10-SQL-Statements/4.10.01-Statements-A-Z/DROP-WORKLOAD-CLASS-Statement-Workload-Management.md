# 4.10.1.113 DROP WORKLOAD CLASS Statement (Workload Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 934–935

Removes workload classes.

## Syntax

```sql
DROP WORKLOAD CLASS <workload_class_name>
```

## Syntax Elements

#### workload_class_name

Removes the specified workload class.

```sql
<workload_class_name> ::= <identifier>
```

## Description

Removes workload classes.

## Permissions

The use of this statement requires the WORKLOAD_ADMIN privilege.

## Examples

Drop the workload class “MyWorkloadClass”.

```sql
DROP WORKLOAD CLASS "MyWorkloadClass";
```

## Related Information

[WORKLOAD_CLASSES System View](../../../6-System-Views-Reference/6.01-System-Views/WORKLOAD_CLASSES-System-View.md)
