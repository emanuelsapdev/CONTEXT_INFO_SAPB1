# 4.10.1.110 DROP USER Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 930–932

Deletes a database user.

## Syntax

```sql
DROP USER <user_name> [<drop_option>]
```

## Syntax Elements

#### user_name

Drops the specified user.

```sql
<user_name> ::= <unicode_name>
```

`<user_name>` must specify an existing database user.

#### drop_option

Specifies the drop option to use.

```sql
<drop_option> ::= CASCADE | RESTRICT
```

CASCADE drops the user and performs the following actions:

- Drops the user's home schema and other schemas belonging to the user, together with all objects stored in them regardless of which user created them.
- Drops all objects owned by the user, even if they are part of another schema.
- Drops objects that are dependent on deleted objects and that are owned by the user being dropped.
- Invalidates objects that are dependent on deleted objects and that are owned by a different user in a schema not belonging to the user being dropped.
- Drops public synonyms that are owned by the user being dropped.
- Revokes privileges on deleted objects.
- Revokes privileges granted by the deleted user. Revoked privileges may cause further revokes if the privileges have been granted further.

RESTRICT drops the user only if they don’t own any schemas or objects other than their home schema. If RESTRICT is specified while the user owns any objects, then an error is returned.

When `<drop_option>` is not specified, RESTRICT is used by default.

## Description

Users created by the deleted user and roles created by them are not deleted.

Audit policies created by the deleted user are not deleted.

It is possible to delete a user even if an open session for this user exists.

The deleted user is deleted in the following views: USERS, USER_PARAMETERS, INVALID_CONNECT_ATTEMPTS

The deletion of objects influence all of the system views describing objects: TABLES, VIEWS, PROCEDURES, and so on.

The deletion of objects influence the view describing privileges like GRANTED_PRIVILEGES and all of the monitoring views like M_RS_TABLES, M_TABLE_LOCATIONS, and so on.

## Permissions

Only database users with the USER ADMIN system privilege can drop a database user. Each user with this privilege is allowed to drop any user. Only those users which are delivered with the SAP HANA database cannot be dropped: SYS, SYSTEM, _SYS_REPO, and _SYS_STATISTICS.

## System Views

## Example

Create a new user called new_user.

```sql
CREATE USER new_user PASSWORD Password1;
```

Drop the user new_user you created in the previous step. As the CASCADE option is used, the user is dropped together with all of the objects belonging to that user.

```sql
DROP USER new_user CASCADE;
```

## Related Information

USERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/USERS-System-View.md) USER_PARAMETERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/USER_PARAMETERS-System-View.md) INVALID_CONNECT_ATTEMPTS System View [→](../../../6-System-Views-Reference/6.01-System-Views/INVALID_CONNECT_ATTEMPTS-System-View.md) M_RS_TABLES System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_RS_TABLES-System-View.md) M_TABLE_LOCATIONS System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_LOCATIONS-System-View.md)
