# 6.2.333 M_TIMEZONE_ALERTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2110–2111

Provides information about alerts relating to the status of SAP HANA internal timezone conversion.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| STATUS | VARCHAR(32) | Displays the status to report: TABLES NOT FOUND, TABLES EMPTY, NO SYS TEM TIMEZONE, SYSTEM TIMEZONE DISABLED, or CONVERSION MIS MATCH. |
| TIMEZONE_NAME | NVARCHAR(64) | Displays the name of the timezone to which status message applies or NULL if the status does not apply to a specific timezone. |
| MISMATCH_BEGIN | TIMESTAMP | Displays the UTC time at which the first mismatch of the mismatch period occurred or NULL if no mismatch applies. |
| MISMATCH_END | TIMESTAMP | Displays the UTC time at which the last mismatch of the mismatch period occurred or NULL if no mismatch applies. |
| DETAILS | NVARCHAR(256) | Displays the detailed information. |

## Related Information

TIMEZONES System View [→](../6.01-System-Views/TIMEZONES-System-View.md) ALTER SYSTEM CLEAR TRACES Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-TRACES-Statement-System-Management.md) ALTER SYSTEM CLEAR TIMEZONE CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-TIMEZONE-CACHE-Statement-System.md) UTCTOLOCAL Function (Datetime) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/UTCTOLOCAL-Function-Datetime.md) LOCALTOUTC Function (Datetime) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LOCALTOUTC-Function-Datetime.md)
