# 4.10.1.19.20 ALTER SYSTEM CLEAR AUDIT LOG Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 504–505

Deletes old audit data from the SAP HANA database audit table.

## Syntax

```sql
ALTER SYSTEM CLEAR AUDIT LOG [ FOR AUDIT POLICY <policy_name> ]
<until_specification>
```

## Syntax Elements

#### until_specification

Removes audit data older than the `<timestamp>`.

```sql
<until_specification> ::= { UNTIL <timestamp> | ALL }
<timestamp> ::= <string_literal>
```

If the ALL keyword is used, then all the audit data is removed.

## Description

Use this command to delete old audit data from the SAP HANA database audit table.

## Example

Delete audit log data older than December 31st 2012.

```sql
ALTER SYSTEM CLEAR AUDIT LOG UNTIL '2012-12-31 23:59:59';
```

Delete all audit log data for audit policy MY_POLICY.

```sql
ALTER SYSTEM CLEAR AUDIT LOG FOR AUDIT POLICY MY_POLICY ALL;
```

## Related Information

[AUDIT_LOG System View](../../../../6-System-Views-Reference/6.01-System-Views/AUDIT_LOG-System-View.md)
