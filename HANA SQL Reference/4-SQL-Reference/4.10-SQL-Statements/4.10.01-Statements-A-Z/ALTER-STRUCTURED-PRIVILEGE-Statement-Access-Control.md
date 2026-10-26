# 4.10.1.18 ALTER STRUCTURED PRIVILEGE Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 466–467

Alters a structured (analytic) privilege.

## Syntax

```sql
ALTER STRUCTURED PRIVILEGE <privilege_name> FOR <action>
   ON <object_name_list> <filter_condition>
```

## Syntax Elements

#### privilege_name

Specifies the name of the privilege.

```sql
<privilege_name> ::= [<schema>.]<identifier>
```

#### action

Specifies the action the privilege allows.

```sql
<action> ::= SELECT
```

#### object_name_list

Specifies the views to be restricted by the privilege.

```sql
<object_name_list> ::= <object_name> [{, <object_name>}...]
<object_name> :: = [<schema>.]<identifier>
```

`<object_name>` specifies a view registered for SQL-based analytic privilege check.

#### filter_condition

Restricts the returned rows of the specified views for users who have been granted the privilege.

```sql
<filter_condition> ::=
 <static_filter_condition> | <dynamic_filter_condition>
```

```sql
<static_filter_condition> ::= WHERE <condition>
```

```sql
<dynamic_filter_condition> ::= CONDITION PROVIDER <procedure_name>
<procedure_name> ::= [<schema>.]<identifier>
```

`<condition>` restricts the rows returned and can contain subqueries.

`<procedure_name>` specifies the procedure providing the dynamic restriction.

## Permissions

You must have the STRUCTUREDPRIVILEGE ADMIN privilege to execute this statement.

## Description

Alters an analytic privilege. Analytic privileges provide finegrained control over which data a user can see within a view. Analytic privileges are sometimes referred to as structured privileges.

## Related Information

STRUCTURED_PRIVILEGES System View [→](../../../6-System-Views-Reference/6.01-System-Views/STRUCTURED_PRIVILEGES-System-View.md) DROP STRUCTURED PRIVILEGE Statement (Access Control) [→](DROP-STRUCTURED-PRIVILEGE-Statement-Access-Control.md) CREATE STRUCTURED PRIVILEGE Statement (Access Control) [→](CREATE-STRUCTURED-PRIVILEGE-Statement-Access-Control.md)
