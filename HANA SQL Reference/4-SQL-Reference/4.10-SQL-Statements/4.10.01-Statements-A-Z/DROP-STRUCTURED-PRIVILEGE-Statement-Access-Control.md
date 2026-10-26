# 4.10.1.105 DROP STRUCTURED PRIVILEGE Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 923–924

Drops a structured (analytic) privilege.

## Syntax

```sql
DROP STRUCTURED PRIVILEGE <privilege_name>
```

## Syntax Elements

#### privilege_name

Specifies the name of the analytic privilege to drop.

## Permissions

You must have the STRUCTUREDPRIVILEGE ADMIN privilege to execute this statement.

## Description

Drops an analytic privilege. Analytic privileges provide finegrained control over which data a user can see within a view. Analytic privileges are sometimes referred to as structured privileges.

## Related Information

STRUCTURED_PRIVILEGES System View [→](../../../6-System-Views-Reference/6.01-System-Views/STRUCTURED_PRIVILEGES-System-View.md) ALTER STRUCTURED PRIVILEGE Statement (Access Control) [→](ALTER-STRUCTURED-PRIVILEGE-Statement-Access-Control.md) DROP STRUCTURED PRIVILEGE Statement (Access Control) [→](DROP-STRUCTURED-PRIVILEGE-Statement-Access-Control.md)
