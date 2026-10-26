# 6.1.151 SESSION_COOKIES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1570–1571

Shows information about available session cookies.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USER_NAME | NVARCHAR(256) | Displays the name of the user that the session cookie was created for. |
| CLIENT_HOST | NVARCHAR(64) | Displays the host name of client machine. |
| CLIENT_PID | BIGINT | Displays the client process ID. |
| CREATE_TIME | TIMESTAMP | Displays the time that the session cookie was created. |
| LAST_CONNECT_TIME | TIMESTAMP | Displays the last time that the session cookie was used for successful recon nection. |
| SESSION_END_TIME | TIMESTAMP | Displays the time that the main connection ended. |

## Related Information

[Session Management Statements](../../4-SQL-Reference/4.10-SQL-Statements/4.10.10-Session-Management-Statements.md)

[M_SESSION_CONTEXT System View](../6.02-Monitoring-Views/M_SESSION_CONTEXT-System-View.md)
