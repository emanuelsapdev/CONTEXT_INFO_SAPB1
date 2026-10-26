# 4.10.1.72 CREATE USERGROUP Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 853–855

Creates a usergroup.

## Syntax

```sql
CREATE USERGROUP <usergroup_name>
 [ DISABLE USER ADMIN ]
 [ NO GRANT TO CREATOR ]
 [ SET PARAMETER <parameter_key_value_list> ]
 [ ENABLE PARAMETER SET <parameter_set_name> ]
```

## Syntax Elements

#### usergroup_name

Specifies a name for the usergroup. `<usergroup_name>` cannot match the name of an existing schema, user, usergroup, or role.

#### DISABLE USER ADMIN

Prevents users with USER ADMIN privilege from administering the usergroup (for example, changing settings and adding/removing users).

If DISABLE USER ADMIN is specified, then only users with USERGROUP OPERATOR privilege on the usergroup can administer the usergroup.

#### NO GRANT TO CREATOR

Prevents the automatic granting of all object privileges of the usergroup to the user creating the usergroup.

#### SET PARAMETER parameter_key_value_list

Configures parameter options as a key-value list for a parameter set that can be enabled and disabled for the group. Specifically, use this clause to configure groupspecific values for the individual options of the password policy set called 'password policy'.

```sql
<parameter_key_value_list> ::= <key_value_pair> [,<key_value_pair> [,…] ]
<key_value_pair> ::= '<parameter_name>'='<value>'
```

When the SET PARAMETER clause is used to specify password policy options, all policy option settings are stored for the usergroup with the exception of password_lock_for_system_user, which is not applicable or allowed for usergroups. However, this does not mean you need to specify all of the password policy options. Password policy options that are not specified in the SET PARAMETER clause are copied from the current system-wide password policy settings and stored with the specified options for the usergroup. Subsequent changes to the system-wide settings do not impact any stored password policy options for the usergroup. Refer to the SAP HANA Administration Guide for the list of password policy options you can set.

Once you set the parameter set options, use a ALTER USERGROUP...SET PARAMETER statement to alter specific parameter settings without impacting other parameter settings that have been set.

#### ENABLE PARAMETER SET parameter_set_name

Enables the specified parameter set. The only supported parameter set name is 'password policy'.

```sql
<parameter_set_name> ::= 'password policy'
```

Enabling the password policy parameter causes any password policy options that have been defined to be applied. If ENABLE PARAMETER SET 'password policy' is not specified, any password policy options configured using the SET PARAMETER clause remain configured for the usergroup, but not applied. Also, if a parameter set is enabled before any parameters have been set, all parameter values are identical to the current system wide settings.

## Description

If you create the usergroup with DISABLE USER ADMIN, then you must use the GRANT statement to grant USERGROUP OPERATOR privilege to a user on the usergroup so that they can administer it.

You add users to a usergroup using the CREATE USER and ALTER USER statements.

The M_EFFECTIVE_PASSWORD_POLICY system view can be used to query the current password policy settings for a user.

## Permissions

You must have the USER ADMIN privilege to create a usergroup.

## Example

The following example creates a usergroup called `MyUserGroup` and sets the restriction that only users with USERGROUP OPERATOR privilege on the usergroup can administer it:

```sql
CREATE USERGROUP MyUserGroup DISABLE USER ADMIN NO GRANT TO CREATOR;
```

The following example creates a usergroup called `Training` and sets several password policy options for the usergroup:

```sql
CREATE USERGROUP Training SET PARAMETER 'password_layout' = 'A1a!',
'minimal_password_length' = '16' ENABLE PARAMETER SET 'password policy';
```

## Related Information

ALTER USERGROUP Statement (Access Control) [→](ALTER-USERGROUP-Statement-Access-Control.md) DROP USERGROUP Statement (Access Control) [→](DROP-USERGROUP-Statement-Access-Control.md) GRANT Statement (Access Control) [→](GRANT-Statement-Access-Control.md)

USERGROUPS System View [→](../../../6-System-Views-Reference/6.01-System-Views/USERGROUPS-System-View.md) USERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/USERS-System-View.md) CREATE USER Statement (Access Control) [→](CREATE-USER-Statement-Access-Control.md) USERGROUP_PARAMETERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/USERGROUP_PARAMETERS-System-View.md)
