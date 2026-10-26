# 4.10.1.140 REVOKE Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1030–1033

Revokes roles or privileges for the specified objects from a user or role.

## Syntax

```sql
REVOKE <system_privilege>,... FROM <grantee>
 | REVOKE <source_privilege>,... ON REMOTE SOURCE <source_name> FROM <grantee>
 | REVOKE <schema_privilege>,... ON SCHEMA <schema_name> FROM <grantee>
 | REVOKE <object_privilege>,... ON <object_name> FROM <grantee>
 | REVOKE <column_key_privilege> ON CLIENTSIDE ENCRYPTION COLUMN KEY <key_name>
FROM <grantee>
 | REVOKE <role_name>,... FROM <grantee> [ GRANTED BY <grantor> ]
 | REVOKE STRUCTURED PRIVILEGE <privilege_name> FROM <grantee>
```

## Syntax Elements

For the definition of all of the other syntax elements not listed here, see the GRANT statement.

#### GRANTED BY grantor

Allows a user with the ROLE ADMIN privilege to revoke a role that they did not grant. `<grantor>` specifies the user who granted `<role_name>` to `<grantee>`.

## Permissions

For users without ROLE ADMIN privileges, only the user that granted a specific privilege can revoke it.

## Description

If a user has been granted a role, then you cannot revoke a subset of the privileges belonging to that role. To grant a subset of privileges contained within a role, revoke the entire role and grant the required privileges separately.

Revoking a privilege or role can lead to some views becoming inaccessible or procedures that the user can no longer execute. This situation occurs if a view or procedure depends on a revoked privilege or on one of the privileges the role had.

Revoking a privilege that had been granted with WITH GRANT OPTION or with WITH ADMIN OPTION results in recursive revocation of privileges. Privileges are not only revoked from the user specified in the command, but also from all the users and roles that were granted that privilege directly or indirectly by the specified user.

Privileges can be granted to a user or role by more than one grantor; revocation of a privilege by one grantor user does not necessarily mean that the privilege is revoked from the user or role.

## Example

Create a new user named `worker`.

```sql
CREATE USER worker PASSWORD His_Password_1;
```

Create a new role named `role_for_work_on_my_schema`.

```sql
CREATE ROLE role_for_work_on_my_schema;
```

Create a new schema named `my_schema`.

```sql
CREATE SCHEMA my_schema OWNED BY system;
```

Create a new table named `work_done` in the schema.

```sql
CREATE ROW TABLE my_schema.work_done (t TIMESTAMP, user NVARCHAR (256),
work_done VARCHAR (256));
```

Grant the SELECT privilege on any object privilege in `my_schema` to the role `role_for_work_on_my_schema`.

```sql
GRANT SELECT ON SCHEMA my_schema TO role_for_work_on_my_schema;
```

Grant the INSERT privilege for the `work_done` table to the role `role_for_work_on_my_schema`.

```sql
GRANT INSERT ON my_schema.work_done TO role_for_work_on_my_schema;
```

Grant the `role_for_work_on_my_schema` role to the `worker` user.

```sql
GRANT role_for_work_on_my_schema TO worker;
```

Grant TRACE ADMIN privilege for the `worker` user.

```sql
GRANT TRACE ADMIN TO worker WITH ADMIN OPTION;
```

Grant the DELETE privilege from the `work_done` table to the `worker` user.

```sql
GRANT DELETE ON my_schema.work_done TO worker WITH GRANT OPTION;
```

Revoke from the role `role_for_work_on_my_schema` the privilege to select from `my_schema`.

```sql
REVOKE SELECT ON SCHEMA my_schema FROM role_for_work_on_my_schema;
```

Revoke TRACE ADMIN privilege from the `worker` user.

```sql
REVOKE TRACE ADMIN FROM worker;
```

Revoke the LINKED DATABASE privilege from user `myuser1` using remote source `myremotesys`.

```sql
REVOKE LINKED DATABASE ON REMOTE SOURCE myremotesys FROM myuser1;
```

Revoke the USAGE privilege on encryption key `Key5` from user `bsmith`.

```sql
REVOKE USAGE ON CLIENTSIDE ENCRYPTION COLUMN KEY Key5 FROM bsmith;
```

Revoke the CLIENTSIDE ENCRYPTION COLUMN KEY ADMIN privilege from user `bsmith` on schema `my_schema`.

```sql
REVOKE CLIENTSIDE ENCRYPTION COLUMN KEY ADMIN ON SCHEMA my_schema FROM bsmith;
```

## Related Information

GRANT Statement (Access Control) [→](GRANT-Statement-Access-Control.md) CREATE USER Statement (Access Control) [→](CREATE-USER-Statement-Access-Control.md) ALTER USER Statement (Access Control) [→](ALTER-USER-Statement-Access-Control.md)

USERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/USERS-System-View.md) GRANT Statement (Access Control) [→](GRANT-Statement-Access-Control.md) USERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/USERS-System-View.md) ROLES System View [→](../../../6-System-Views-Reference/6.01-System-Views/ROLES-System-View.md) GRANTED_ROLES System View [→](../../../6-System-Views-Reference/6.01-System-Views/GRANTED_ROLES-System-View.md) GRANTED_PRIVILEGES System View [→](../../../6-System-Views-Reference/6.01-System-Views/GRANTED_PRIVILEGES-System-View.md)
