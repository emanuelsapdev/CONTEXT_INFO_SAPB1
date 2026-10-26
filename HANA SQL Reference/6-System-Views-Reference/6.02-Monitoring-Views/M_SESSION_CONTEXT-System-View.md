# 6.2.266 M_SESSION_CONTEXT System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2007–2008

Displays the session variables set for each connection.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| CONNECTION_ID | INTEGER | Displays the connection ID. |
| KEY | VARCHAR(32) | Displays the key name of a session con text variable. |
| VALUE | NVARCHAR(512) | Displays the value of a session context variable. |
| SECTION | VARCHAR(8) | Displays the section name to distinguish system and user variables:<br>• USER=application defined variable using SET command or client API call.<br>• SYSTEM=predefined variable or server property. |

## Additional Information

Execute the following statement to view the assigned session variables for the current connection:

```sql
SELECT * FROM M_SESSION_CONTEXT WHERE connection_id=current_connection;
```

## Related Information

SET [SESSION] Statement (Session Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/SET-SESSION-Statement-Session-Management.md) SESSION_CONTEXT Function (Miscellaneous) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/SESSION_CONTEXT-Function-Miscellaneous.md) Session Variables [→](../../4-SQL-Reference/4.08-Session-Variables.md) Session Management Statements [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.10-Session-Management-Statements.md)
