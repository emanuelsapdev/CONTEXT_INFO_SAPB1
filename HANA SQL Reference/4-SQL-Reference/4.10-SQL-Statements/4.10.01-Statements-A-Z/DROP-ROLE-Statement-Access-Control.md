# 4.10.1.99 DROP ROLE Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 913–914

Drops a role.

## Syntax

```sql
DROP ROLE <role_name>
```

## Syntax Elements

#### role_name

Drops the specified role, with the optional schema name.

```sql
<role_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

`<role_name>` must specify an existing role.

## Description

Roles that are delivered with the SAP HANA database cannot be dropped: PUBLIC, CONTENT_ADMIN, MODELING, MONITORING, and SAP_INTERNAL_HANA_SUPPORT.

If a role has been granted to a user or another role, then it is revoked when the role is dropped. Revoking a role may lead to making some views inaccessible or making procedures not executable, which occurs if a view or procedures depends on any of the privileges of the dropped role.

Note that when dropping a role mapped to an LDAP group, in addition to revoking the role from users to whom it was granted, its mapping to LDAP group is deleted.

## Permissions

Only database users with the ROLE ADMIN system privilege can drop a role. Each user that has this privilege is allowed to drop any role.

## Example

Create a role with the name role_for_work_on_my_schema.

```sql
CREATE ROLE role_for_work_on_my_schema;
```

Drop the role_for_work_on_my_schema role.

```sql
DROP ROLE role_for_work_on_my_schema;
```

## Related Information

ALTER ROLE Statement (Access Control) [→](ALTER-ROLE-Statement-Access-Control.md) CREATE ROLE Statement (Access Control) [→](CREATE-ROLE-Statement-Access-Control.md) ROLES System View [→](../../../6-System-Views-Reference/6.01-System-Views/ROLES-System-View.md) GRANTED_ROLES System View [→](../../../6-System-Views-Reference/6.01-System-Views/GRANTED_ROLES-System-View.md) GRANTED_PRIVILEGES System View [→](../../../6-System-Views-Reference/6.01-System-Views/GRANTED_PRIVILEGES-System-View.md)
