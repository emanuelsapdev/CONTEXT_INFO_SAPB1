# 4.10.1.102 DROP SCHEMA SYNONYM Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 917–918

Removes a schema synonym.

## Syntax

```sql
DROP SCHEMA SYNONYM <synonym_name>
```

## Syntax Elements

**synonym_name** The name of the schema synonym to drop.

## Description

Use DROP SCHEMA SYNONYM to remove a schema synonym.

## Permissions

You must have the CREATE SCHEMA system privilege.

A schema synonym is automatically dropped when the schema to which it refers is dropped.

## Example

Execute the following statement to create a schema synonym called TEST_SCHEMA_SYN that references the schema SYSTEM:

```sql
CREATE OR REPLACE SCHEMA SYNONYM TEST_SCHEMA_SYN FOR SYSTEM;
```

Execute the next statement to drop that same schema synonym:

```sql
DROP SCHEMA SYNONYM TEST_SCHEMA_SYN;
```

## Related Information

DROP SCHEMA Statement (Data Definition) [→](DROP-SCHEMA-Statement-Data-Definition.md) CREATE SCHEMA Statement (Data Definition) [→](CREATE-SCHEMA-Statement-Data-Definition.md) CREATE SCHEMA SYNONYM Statement (Data Definition) [→](CREATE-SCHEMA-SYNONYM-Statement-Data-Definition.md) SET SCHEMA Statement (Session Management) [→](SET-SCHEMA-Statement-Session-Management.md)
