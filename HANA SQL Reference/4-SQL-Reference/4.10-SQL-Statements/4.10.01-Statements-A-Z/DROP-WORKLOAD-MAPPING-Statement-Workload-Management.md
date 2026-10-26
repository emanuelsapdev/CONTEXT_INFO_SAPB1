# 4.10.1.114 DROP WORKLOAD MAPPING Statement (Workload Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 935–936

Drops a workload mapping.

## Syntax

```sql
DROP WORKLOAD MAPPING <mapping_name>
```

## Syntax Elements

#### mapping_name

Specifies the workload mapping to drop.

```sql
<mapping_name> ::= <identifier>
```

## Description

Drops a workload mapping.

## Permissions

The use of this statement requires the WORKLOAD_ADMIN privilege.

## Examples

Remove the workload mapping "MyWorkloadMapping".

```sql
DROP WORKLOAD MAPPING "MyWorkloadMapping";
```

## Related Information

[WORKLOAD_MAPPINGS System View](../../../6-System-Views-Reference/6.01-System-Views/WORKLOAD_MAPPINGS-System-View.md)
