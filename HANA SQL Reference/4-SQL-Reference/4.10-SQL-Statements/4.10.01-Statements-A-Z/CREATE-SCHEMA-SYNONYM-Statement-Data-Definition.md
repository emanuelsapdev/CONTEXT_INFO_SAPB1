# 4.10.1.63 CREATE SCHEMA SYNONYM Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 762–763

Creates a schema synonym.

## Syntax

```sql
CREATE [OR REPLACE] SCHEMA SYNONYM <synonym_name> FOR <schema_reference>
```

## Syntax Elements

#### synonym_name

The name of the synonym.

#### schema_reference

The name of the schema the synonym is for.

## Description

The CREATE SCHEMA SYNONYM statement creates a synonym for an existing schema. Use the synonym when executing the SET SCHEMA statement, and, at connection time, the schema is redirected to the schema referenced by the synonym.

The synonym name cannot be the same as an existing schema name.

## Permissions

You must have the CREATE SCHEMA system privilege.

## Example

Execute the following statement to create a schema synonym called TEST_SCHEMA_SYN that references the schema SYSTEM:

```sql
CREATE SCHEMA SYNONYM TEST_SCHEMA_SYN FOR SYSTEM;
```

Execute the next statement to set the schema to the new schema synonym at connection time:

```sql
SET SCHEMA TEST_SCHEMA_SYN;
```

Now, when you execute `SELECT CURRENT_SCHEMA FROM DUMMY;`, it returns SYSTEM.

Execute the following statement to change the target schema from the schema synonym TEST_SCHEMA_SYN to the actual schema SYSTEM:

```sql
SET SCHEMA SYSTEM;
```

If you execute `SELECT CURRENT_SCHEMA FROM DUMMY;` again, it returns SYSTEM.

## Related Information

SET SCHEMA Statement (Session Management) [→](SET-SCHEMA-Statement-Session-Management.md) DROP SCHEMA Statement (Data Definition) [→](DROP-SCHEMA-Statement-Data-Definition.md) DROP SCHEMA SYNONYM Statement (Data Definition) [→](DROP-SCHEMA-SYNONYM-Statement-Data-Definition.md) CREATE SCHEMA Statement (Data Definition) [→](CREATE-SCHEMA-Statement-Data-Definition.md)
