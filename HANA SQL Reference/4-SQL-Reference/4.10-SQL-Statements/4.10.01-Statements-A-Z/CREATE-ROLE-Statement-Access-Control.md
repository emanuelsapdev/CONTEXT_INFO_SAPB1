# 4.10.1.60 CREATE ROLE Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 757–759

Creates a new role.

## Syntax

```sql
CREATE ROLE <role_name> [ LDAP GROUP <ldap_group_list> ] [ NO GRANT TO CREATOR ]
```

## Syntax Elements

#### role_name

Specifies the name of the role to be created with optional schema name.

```sql
<role_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

The name must not be identical to the name of an existing user or role. If no schema is specified, then a global role is created. If you specify a schema as part of the role name, then the role name is local to that schema only and does not collide with roles with the same name in other schemas or in the global namespace. Dropping a schema drops all roles contained in the namespace of that schema.

#### ldap_group_list

Specifies the Distinguished Name (DN) of one or more LDAP groups.

```sql
<ldap_group_list> ::= <ldap_group_name> [,...]
<ldap_group_name> ::= <string_literal>
```

A local role mapped to an LDAP group can also be granted to another role or a user as before. Note that when dropping an LDAP-mapped role using DROP ROLE, in addition to revoking the role from users to whom it was granted, its mapping to the LDAP group is deleted.

#### NO GRANT TO CREATOR

Prevents the automatic granting of the role to the user creating the role

## Description

For a list of system roles provided in the SAP HANA database, see the GRANT statement. To see all roles, including custom roles that have been created using the CREATE ROLE statement, query the ROLES system view. To view which roles and privileges have actually been granted, query the GRANTED_ROLES and GRANTED_PRIVILEGES system views, respectively.

## Permissions

Only database users with the ROLE ADMIN system privilege can create roles.

## Example

Create a role with the name role_for_work_on_my_schema:

```sql
CREATE ROLE role_for_work_on_my_schema NO GRANT TO CREATOR;
```

Create a role and associated it with an LDAP group:

```sql
CREATE ROLE Securities_DBA
 LDAP GROUP
'cn=Securities_DBA,OU=Application,OU=Groups,ou=DatabaseAdmins,cn=Users,o=largeban
k.com';
```
