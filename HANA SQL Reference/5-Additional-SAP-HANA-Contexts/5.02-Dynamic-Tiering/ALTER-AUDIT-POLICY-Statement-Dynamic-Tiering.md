# 5.2.1 ALTER AUDIT POLICY Statement [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1216–1218

Enables or disables an audit policy.

## Syntax

```sql
ALTER AUDIT POLICY <policy_name> [
  <audit_mode>
  | <set_audit_trail_type>
  | <reset_audit_trail_type>
```

## Syntax Elements

#### policy_name

Specifies the name of the audit policy to be altered.

```sql
<policy_name> ::= <identifier>
```

#### audit_mode

Enables or disables the audit policy.

```sql
<audit_mode> ::= ENABLE | DISABLE
```

##### ENABLE

Enables the audit policy.

##### DISABLE

Disables the audit policy.

#### set_audit_trail_type

Specifies the audit trail target(s) for the audit policy.

```sql
<set_audit_trail_type> ::= SET TRAIL TYPE <audit_trail_type_list>
<audit_trail_type_list> ::= <audit_trail_type_name>[{,
<audit_trail_type_name>}...]
<audit_trail_type_name> ::= SYSLOG
```

#### reset_audit_trail_type

Resets the audit trail target type(s) to the system default.

```sql
<reset_audit_trail_type> ::= RESET TRAIL TYPE
```

## Permissions

You must have the AUDIT ADMIN privilege.

## Description

The ALTER AUDIT POLICY statement enables or disables an audit policy. `<policy_name>` must specify an existing audit policy. Only database users with the system privilege AUDIT ADMIN are allowed to alter an audit policy. Users with this privilege can alter any audit policy, regardless of if they are the creator of the policy.

When an audit policy is created, it is created in the disabled state. Therefore the audit policy has to be enabled to make its audit actions take effect.

An audit policy can be disabled and enabled as often as required.

One or more audit trail targets could be specified for an audit policy at the time of creation (see CREATE AUDIT POLICY Statement [Dynamic Tiering] [→](CREATE-AUDIT-POLICY-Statement-Dynamic-Tiering.md)) or after creation.

The allowed audit trail targets are:

- SYSLOG: uses the system syslog
- TABLE: stores audit information in database table. The audit log is accessible using AUDIT_LOG system view
- CSV: stores audit information as comma-separated values in a text file. Should be used only for testing purposes.

## Example

For this example, you need to first create an audit policy called `ext_store_admin_policy` using the following statement.

```sql
 CREATE AUDIT POLICY ext_store_admin_policy CREATE EXTENDED STORAGE, ALTER
EXTENDED STORAGE, DROP EXTENDED STORAGE LEVEL CRITICAL
```

You enable the `ext_store_admin_policy` policy.

```sql
ALTER AUDIT POLICY ext_store_admin_policy ENABLE;
```

You disable the `ext_store_admin_policy` audit policy.

```sql
ALTER AUDIT POLICY ext_store_admin_policy DISABLE;
```

## Related Information

[AUDIT_POLICIES System View](../../6-System-Views-Reference/6.01-System-Views/AUDIT_POLICIES-System-View.md)

M_INIFILE_CONTENTS System View [→](../../6-System-Views-Reference/6.02-Monitoring-Views/M_INIFILE_CONTENTS-System-View.md) AUDIT_LOG System View [→](../../6-System-Views-Reference/6.01-System-Views/AUDIT_LOG-System-View.md) AUDIT_POLICIES System View [→](../../6-System-Views-Reference/6.01-System-Views/AUDIT_POLICIES-System-View.md) AUDIT_LOG System View [→](../../6-System-Views-Reference/6.01-System-Views/AUDIT_LOG-System-View.md) M_INIFILE_CONTENTS System View [→](../../6-System-Views-Reference/6.02-Monitoring-Views/M_INIFILE_CONTENTS-System-View.md)
