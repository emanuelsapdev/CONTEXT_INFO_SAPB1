# 4.10.1.111 DROP USERGROUP Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 932–933

Removes a user group from the database.

## Syntax

```sql
DROP USERGROUP <usergroup_name>
```

## Syntax Elements

#### usergroup_name

The name of the user group.

## Description

You must remove all users from the user group before you can drop it. An error is returned if you attempt to drop a user group that still has users.

## Permissions

You must have the USER ADMIN privilege to drop a user group.

## Example

The following statement drops a (fictitious) user group named `MyUserGroup`;

```sql
DROP USERGROUP MyUserGroup;
```

## Related Information

ALTER USER Statement (Access Control) [→](ALTER-USER-Statement-Access-Control.md) CREATE USERGROUP Statement (Access Control) [→](CREATE-USERGROUP-Statement-Access-Control.md) ALTER USERGROUP Statement (Access Control) [→](ALTER-USERGROUP-Statement-Access-Control.md)

[USERGROUPS System View](../../../6-System-Views-Reference/6.01-System-Views/USERGROUPS-System-View.md)
