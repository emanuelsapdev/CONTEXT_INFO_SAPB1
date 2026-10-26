# 4.10.1.19.23 ALTER SYSTEM CLEAR INIFILE CONTENT HISTORY Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 507–508

Clears `ini` file content history from the catalog.

## Syntax

```sql
ALTER SYSTEM CLEAR INIFILE CONTENT HISTORY
```

## Description

When you use this statement, the specified `ini` file catalog history data is cleared from the M_INIFILE_CONTENT_HISTORY system view and underlying table.

In addition to deleting the records of `ini` file changes, this statement also inserts a record into M_INIFILE_CONTENT_HISTORY to indicate the operation.

## Permissions

You must have the MONITOR ADMIN privilege to execute this statement.

## Related Information

M_INIFILE_CONTENTS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_INIFILE_CONTENTS-System-View.md) M_INIFILE_CONTENT_HISTORY System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_INIFILE_CONTENT_HISTORY-System-View.md) M_INIFILES System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_INIFILES-System-View.md)
