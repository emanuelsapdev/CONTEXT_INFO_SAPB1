# 4.10.1.14 ALTER ROLE Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 452–453

Adds and drops the mapping of LDAP groups for a role.

## Syntax

```sql
ALTER ROLE <role_name>
 ADD LDAP GROUP <ldap_group_list>
 | DROP LDAP GROUP <ldap_group_list>
```

## Syntax Elements

#### role_name

Specifies the name of the role to be altered with optional schema name.

```sql
<role_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### ldap_group_list

Specifies the Distinguished Name (DN) of one or more LDAP groups.

```sql
<ldap_group_list> ::= <ldap_group_name> [,...]
<ldap_group_name> ::= <string_literal>
```

## Description

A local role mapped to an LDAP group can also be granted to another role or a user.

For a list of system roles provided in the SAP HANA database, see the GRANT statement. To see all roles, including custom roles that have been created using the CREATE ROLE statement, query the ROLES system view. To view which roles and privileges have actually been granted, query the GRANTED_ROLES and GRANTED_PRIVILEGES system views, respectively.

## Permissions

Only database users with the ROLE ADMIN system privilege can alter roles.

## Examples

Alter a role associated with an LDAP group:

```sql
ALTER ROLE Securities_DBA
   ADD LDAP GROUP
'cn=Securities_DBA,OU=Application,OU=Groups,ou=DatabaseAdmins,cn=Users,o=verylarg
ebank.com';
```

## Related Information

CREATE ROLE Statement (Access Control) [→](CREATE-ROLE-Statement-Access-Control.md) DROP ROLE Statement (Access Control) [→](DROP-ROLE-Statement-Access-Control.md) ROLES System View [→](../../../6-System-Views-Reference/6.01-System-Views/ROLES-System-View.md) GRANTED_ROLES System View [→](../../../6-System-Views-Reference/6.01-System-Views/GRANTED_ROLES-System-View.md) GRANTED_PRIVILEGES System View [→](../../../6-System-Views-Reference/6.01-System-Views/GRANTED_PRIVILEGES-System-View.md)
