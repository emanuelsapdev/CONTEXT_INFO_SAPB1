# 6.2.363 M_XS_SESSIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2159–2161

Provides information about sessions running in SAP HANA XS.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| XS_SESSION_ID | BIGINT | Displays the identifier of XS session running on this host. |
| USER_NAME | NVARCHAR(256) | Displays the user name. |
| REQUEST_COUNT | INTEGER | Displays the number of HTTP requests that invoked this XS session. |
| AUTHENTICATION_METHOD | VARCHAR(48) | Displays the method used for authenticating this XS session |
| IS_DEBUGGED | VARCHAR(5) | Displays whether a debugger is currently attached to this XS session: TRUE/FALSE. |
| REFERENCE_COUNT | INTEGER | Displays the current number of references to this XS session. |
| START_TIME | TIMESTAMP | Displays the point in time when this XS session started. |
| LAST_REQUEST_TIME | TIMESTAMP | Displays the point in time of last activity in the XS session. |

## Related Information

SET [SESSION] Statement (Session Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/SET-SESSION-Statement-Session-Management.md) UNSET [SESSION] Statement (Session Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/UNSET-SESSION-Statement-Session-Management.md)
