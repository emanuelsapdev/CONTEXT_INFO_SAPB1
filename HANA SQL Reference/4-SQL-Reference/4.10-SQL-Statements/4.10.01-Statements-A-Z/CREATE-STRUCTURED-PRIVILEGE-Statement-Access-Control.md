# 4.10.1.66 CREATE STRUCTURED PRIVILEGE Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 775–776

Creates a structured (analytic) privilege.

## Syntax

```sql
CREATE STRUCTURED PRIVILEGE <privilege_name> FOR <action>
   ON <object_name_list> <filter_condition>
```

## Syntax Elements

#### privilege_name

Specifies a name for the privilege.

```sql
<privilege_name> ::= [<schema>.]<identifier>
```

#### action

```sql
<action> ::= SELECT
```

#### object_name_list

Specifies the views to be restricted by this analytic privilege.

```sql
<object_name_list> ::= <object_name> [{, <object_name>}...]
<object_name> :: = [<schema>.]<identifier>
```

`<object_name>` specifies a view registered for a SQL-based analytic privilege check.

#### filter_condition

Restricts the returned rows of the specified views for users who have been granted this privilege.

```sql
<filter_condition> ::= <static_filter_condition> | <dynamic_filter_condition>
<static_filter_condition> ::= WHERE <condition>
<dynamic_filter_condition> ::= CONDITION PROVIDER <procedure_name>
<procedure_name> ::= [<schema>.]<identifier>
```

`<condition>` restricts the rows returned and can contain subqueries.

`<procedure_name>` specifies the procedure providing the dynamic restriction.

## Description

Creates an analytic privilege. Analytic privileges provide finegrained control over which data a user can see within a view. Analytic privileges are also referred to as structured privileges.

The new structured privilege is automatically applied to the owner/creator of the privilege; however, the owner is not listed as a grantee of the privilege in the GRANTED_PRIVILEGES system view because they have the privilege applied to them by virtue of ownership.

## Permissions

You must have the CREATE STRUCTURED PRIVILEGE or STRUCTUREDPRIVILEGE ADMIN privilege to execute this statement.

## Related Information

STRUCTURED_PRIVILEGES System View [→](../../../6-System-Views-Reference/6.01-System-Views/STRUCTURED_PRIVILEGES-System-View.md) ALTER STRUCTURED PRIVILEGE Statement (Access Control) [→](ALTER-STRUCTURED-PRIVILEGE-Statement-Access-Control.md) DROP STRUCTURED PRIVILEGE Statement (Access Control) [→](DROP-STRUCTURED-PRIVILEGE-Statement-Access-Control.md)
