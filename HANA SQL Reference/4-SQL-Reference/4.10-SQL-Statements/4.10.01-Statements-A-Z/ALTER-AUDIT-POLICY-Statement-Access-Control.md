# 4.10.1.1 ALTER AUDIT POLICY Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 416–419

Enables or disables an audit policy, changes audit trail target types for an audit policy, and configures the retention period of the policy.

## Syntax

```sql
ALTER AUDIT POLICY <policy_name>
{ [ FOR <database_name> ] <audit_mode>
   | <set_audit_trail_type>
   | <reset_audit_trail_type>
   | <set_audit_trail_retention>
   | <reset_audit_trail_retention>}
```

## Syntax Elements

#### policy_name

Specifies the name of the audit policy to be altered.

```sql
<policy_name> ::= <identifier>
```

**database_name** Defines the name of the tenant the audit policy is applied to. This option can only be used on SYSTEMDB, not on a tenant in conjunction with the `<audit_mode>` option.

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

Specifies the audit trail target types for the audit policy.

```sql
<set_audit_trail_types> ::= SET TRAIL TYPE <audit_trail_type_list>
<audit_trail_type_list> ::= <audit_trail_type_name> [,
<audit_trail_type_name> [,...] ]
<audit_trail_type_name> ::=
TABLE  [ RETENTION <duration> ]
| SYSLOG
| CSV
```

Specifying CSV on a production system has security implications: users with the DATA ADMIN, CATALOG READ, TRACE ADMIN, or INIFILE ADMIN privilege are able to access the CSV file.

**duration** Specifies the length of time the policy is retained, expressed in days. The value specified in the CREATE or ALTER AUDIT POLICY statement must be greater than the value specified for the minimal_retention_period parameter in the auditing configuration section of the global.ini file. An error is generated if the value is less. The minimal_retention_period parameter value must be between 7 and 3653 (10 years). This limitation does not apply to the duration value in the CREATE or ALTER AUDIT POLICY statement.

#### reset_audit_trail_type

Resets the audit trail target type(s) to the system default.

```sql
<reset_audit_trail_type> ::= RESET TRAIL TYPE
```

#### set_audit_trail_retention

Specifies the length of time the audit entries are retained.

```sql
<set_audit_trail_retention> ::= SET RETENTION <duration>
```

#### reset_audit_trail_retention

Resets the audit trail retention period to the default, which is forever.

```sql
<reset_audit_trail_retention> ::= RESET RETENTION
```

> **Note**
>
> If the retention period is changed, any audit entries that are no longer included are deleted immediately.

## Description

The ALTER AUDIT POLICY statement enables or disables an audit policy. `<policy_name>` must specify an existing audit policy. Only database users with the AUDIT ADMIN privilege are allowed to alter an audit policy. Users with this privilege can alter any audit policy, regardless of if they are the creator of the policy.

New audit policies are disabled by default and must be enabled before the audit actions begin. The configuration parameter global_auditing_state must also be set to true.

An audit policy can be disabled and enabled as often as required.

Specify one or more audit trail targets for an audit policy at the time of creation. The allowed audit trail targets are:

- SYSLOG: uses the system syslog.
- TABLE: stores audit information in database table. The audit log is accessible using AUDIT_LOG system view.
- CSV: stores audit information as comma-separated values in a text file. Use only for testing purposes.

## Permissions

To alter an audit policy on SYSTEMDB or on a tenant, you must have the AUDIT ADMIN privilege.

To use the FOR `<database_name>` option, you need the DATABASE AUDIT ADMIN privilege granted on SYSTEMDB, not on the tenant.

## Example

Create an audit policy called priv_audit by using the following statement.

```sql
CREATE AUDIT POLICY "priv_audit"
   AUDITING SUCCESSFUL
   GRANT PRIVILEGE, REVOKE PRIVILEGE, GRANT ROLE, REVOKE ROLE LEVEL CRITICAL;
```

Enable the priv_audit audit policy.

```sql
ALTER AUDIT POLICY "priv_audit" ENABLE;
```

Set SYSLOG and TABLE as audit trail targets for the priv_audit audit policy.

```sql
ALTER AUDIT POLICY "priv_audit" SET TRAIL TYPE SYSLOG, TABLE;
```

Reset audit trail targets for the priv_audit audit policy.

```sql
ALTER AUDIT POLICY "priv_audit" RESET TRAIL TYPE;
```

Disable the priv_audit audit policy.

```sql
ALTER AUDIT POLICY "priv_audit" DISABLE;
```

Set the retention period for the priv_audit policy to 30 days.

```sql
ALTER AUDIT POLICY "priv_audit" SET RETENTION 30;
```

Remove the retention period for the priv_audit policy.

```sql
ALTER AUDIT POLICY "priv_audit" RESET RETENTION;
```

Enable the audit policy SYSTEMDB_TEST, which was created on the SYSTEMDB and applies the tenant HA2 only.

```sql
ALTER AUDIT POLICY SYSTEMDB_TEST FOR HA2 ENABLE;
```

## Related Information

AUDIT_POLICIES System View [→](../../../6-System-Views-Reference/6.01-System-Views/AUDIT_POLICIES-System-View.md) CREATE AUDIT POLICY Statement (Access Control) [→](CREATE-AUDIT-POLICY-Statement-Access-Control.md)

CREATE AUDIT POLICY Statement (Access Control) [→](CREATE-AUDIT-POLICY-Statement-Access-Control.md) AUDIT_POLICIES System View [→](../../../6-System-Views-Reference/6.01-System-Views/AUDIT_POLICIES-System-View.md) M_INIFILE_CONTENTS System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_INIFILE_CONTENTS-System-View.md) AUDIT_LOG System View [→](../../../6-System-Views-Reference/6.01-System-Views/AUDIT_LOG-System-View.md)
