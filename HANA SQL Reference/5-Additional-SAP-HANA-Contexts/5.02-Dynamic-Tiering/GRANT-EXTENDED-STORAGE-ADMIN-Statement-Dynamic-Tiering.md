# 5.2.28 GRANT EXTENDED STORAGE ADMIN Statement [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1331–1333

Grants the EXTENDED STORAGE ADMIN system privilege required to manage dynamic tiering and create extended storage.

## Syntax

```sql
GRANT EXTENDED STORAGE ADMIN TO <grantee> [WITH ADMIN OPTION]
```

## Syntax Elements

#### WITH ADMIN OPTION

Specifies that the granted privileges can be granted further by the specified user or by those users having the specified role.

## Permissions

You must have the EXTENDED STORAGE ADMIN privilege.

## Description

The EXTENDED STORAGE ADMIN system privilege is required to manage SAP HANA dynamic tiering and create extended storage.

The specified users, roles, objects, and structured privileges have to exist before they can be used in the GRANT command.

To use the GRANT command to grant privileges to other users and roles, a user needs the privilege and also the permissions required to grant that privilege.

Users cannot grant a privilege to themselves.

## System Views

USERS : All users, their creator, creation date and some information about their current status.

ROLES : All roles, their creator and creation date.

GRANTED_ROLES : Roles that are granted to users or roles.

GRANTED_PRIVILEGES : Privileges that are granted to users or roles.

## Examples

You grant the EXTENDED STORAGE ADMIN privilege to the `user` worker. You grant these privileges along with the permission for the worker user to grant them further.

```sql
GRANT EXTENDED STORAGE ADMIN TO worker WITH ADMIN OPTION;
```

## Related Information

GRANT Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/GRANT-Statement-Access-Control.md) USERS System View [→](../../6-System-Views-Reference/6.01-System-Views/USERS-System-View.md) ROLES System View [→](../../6-System-Views-Reference/6.01-System-Views/ROLES-System-View.md) GRANTED_ROLES System View [→](../../6-System-Views-Reference/6.01-System-Views/GRANTED_ROLES-System-View.md) GRANTED_PRIVILEGES System View [→](../../6-System-Views-Reference/6.01-System-Views/GRANTED_PRIVILEGES-System-View.md)
