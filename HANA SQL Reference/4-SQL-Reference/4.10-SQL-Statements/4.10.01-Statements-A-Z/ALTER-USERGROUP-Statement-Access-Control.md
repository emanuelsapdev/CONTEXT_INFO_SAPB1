# 4.10.1.22 ALTER USERGROUP Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 633–636

Alters a usergroup.

## Syntax

```sql
ALTER USERGROUP <usergroup_name>
 { ENABLE | DISABLE } USER ADMIN
 [ SET PARAMETER <parameter_key_value_list> ]
 [ CLEAR PARAMETER <parameter_name_list> ]
 [ { ENABLE | DISABLE } PARAMETER SET <parameter_set_name> ]
```

## Syntax Elements

#### usergroup_name

Specifies the name of the usergroup.

#### { ENABLE | DISABLE } USER ADMIN

Controls whether a user with USER ADMIN privilege can administer the usergroup (change its settings, and add/remove users).

Users with USERGROUP OPERATOR privilege on the usergroup can always administer the usergroup. ENABLE USER ADMIN allows any user with USER ADMIN privilege to administer the group in addition to users with USERGROUP OPERATOR privilege on the usergroup.

DISABLE USER ADMIN allows only users with the USERGROUP OPERATOR privilege on the usergroup to administer the group.

#### SET PARAMETER parameter_key_value_list

Configures parameter options as a key-value list for a parameter set that can be enabled and disabled for the group. Specifically, use this clause to configure groupspecific values for the individual options of the password policy set called 'password policy'.

```sql
<parameter_key_value_list> ::= <key_value_pair> [,<key_value_pair> [,…] ]
<key_value_pair> ::= '<parameter_name>'='<value>'
```

When the SET PARAMETER clause is used to specify password policy options, all policy option settings are stored for the usergroup with the exception of password_lock_for_system_user, which is not applicable or allowed for usergroups. However, this does not mean you need to specify all of the password policy options. Password policy options that are not specified in the SET PARAMETER clause are copied from the current system-wide password policy settings and stored with the specified options for the usergroup. Subsequent changes to the system-wide settings do not impact any stored password policy options for the usergroup. Refer to the SAP HANA Administration Guide for the list of password policy options you can set.

Once you set the parameter set options, use a ALTER USERGROUP...SET PARAMETER statement to alter specific parameter settings without impacting other parameter settings that have been set.

#### CLEAR PARAMETER parameter_name_list

Resets the specified parameter(s) to the current system-wide setting.

```sql
<parameter_name_list> ::= <parameter_name> [, <parameter_name> [,..] ]
```

#### ENABLE PARAMETER SET parameter_set_name

Enables the specified parameter set. The only supported parameter set name is 'password policy'.

```sql
<parameter_set_name> ::= 'password policy'
```

Enabling the password policy parameter causes any password policy options that have been defined to be applied. If ENABLE PARAMETER SET 'password policy' is not specified, any password policy options configured using the SET PARAMETER clause remain configured for the usergroup, but not applied. Also, if a parameter set is enabled before any parameters have been set, all parameter values are identical to the current system wide settings.

#### DISABLE PARAMETER SET parameter_set_name

Disables the specified parameter set. Parameters that have been set remain stored for the usergroup but are not applied. The only supported parameter set name is 'password policy'.

```sql
<parameter_set_name> ::= 'password policy'
```

## Description

To see the groupspecific values of parameters, query the USERGROUP_PARAMETERS system view. To see which values are currently in effect for a particular user, query the M_EFFECTIVE_PASSWORD_POLICY system view.

You add users to a usergroup using the CREATE USER statement.

The M_EFFECTIVE_PASSWORD_POLICY system view can be used to query the current password policy settings for a user.

## Permissions

Only users with USER ADMIN privilege can specify ENABLE/DISABLE USER ADMIN.

For other changes, if the current setting for the usergroup is DISABLE USER ADMIN, then only users with the USERGROUP OPERATOR privilege on the usergroup can alter the group. Otherwise, any user with the USER ADMIN privilege can alter the usergroup, in addition to any user with the USERGROUP OPERATOR privilege on the usergroup.

## Example

The following statement alters the usergroup `MyUserGroup` to allow any user with USER ADMIN privilege to administer it:

```sql
ALTER USERGROUP MyUserGroup ENABLE USER ADMIN;
```

The following example disables the password policy parameter set for the `Training` usergroup:

```sql
ALTER USERGROUP Training DISABLE PARAMETER SET 'password policy';
```

## Related Information

CREATE USERGROUP Statement (Access Control) [→](CREATE-USERGROUP-Statement-Access-Control.md) DROP USERGROUP Statement (Access Control) [→](DROP-USERGROUP-Statement-Access-Control.md) GRANT Statement (Access Control) [→](GRANT-Statement-Access-Control.md) USERGROUPS System View [→](../../../6-System-Views-Reference/6.01-System-Views/USERGROUPS-System-View.md) USERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/USERS-System-View.md) CREATE USER Statement (Access Control) [→](CREATE-USER-Statement-Access-Control.md) USERGROUP_PARAMETERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/USERGROUP_PARAMETERS-System-View.md)
