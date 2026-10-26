# 4.10.1.82 DROP AUDIT POLICY Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 893–894

Drops an audit policy.

## Syntax

```sql
DROP AUDIT POLICY <policy_name> [ FOR <database_name> ]
```

## Syntax Elements

#### policy_name

Specifies the name of the audit policy to be dropped.

```sql
<policy_name> ::= <identifier>
```

`<policy_name>` must specify an existing audit policy. **database_name** Defines the name of the tenant to drop the audit policy to. This option can only be used on SYSTEMDB.

## Description

Even if an audit policy is dropped, the audit action specified in the dropped audit policy can be audited further. This happens if another audit policy is enabled that specifies the dropped audit action.

To temporarily stop auditing an audit policy, disable it.

Since there is no automatic deletion of audit log entries for deleted policies, audit log entries created by such a policy need to be cleaned up manually.

## Permissions

To drop an audit policy on SYSTEMDB or on a tenant, you must have the AUDIT ADMIN privilege.

To use the FOR `<database_name>` option, you need the DATABASE AUDIT ADMIN privilege granted on SYSTEMDB, not on the tenant.

## Example

Create the priv_audit audit policy.

```sql
CREATE AUDIT POLICY priv_audit AUDITING SUCCESSFUL GRANT PRIVILEGE, REVOKE
PRIVILEGE, GRANT ROLE, REVOKE ROLE LEVEL CRITICAL;
```

Drop the priv_audit audit policy.

```sql
DROP AUDIT POLICY priv_audit;
```

Drop the priv_audit1 audit policy on SYSTEMDB for tenant HA2.

```sql
DROP AUDIT POLICY priv_audit1 FOR HA2;
```

## Related Information

[AUDIT_POLICIES System View](../../../6-System-Views-Reference/6.01-System-Views/AUDIT_POLICIES-System-View.md)
