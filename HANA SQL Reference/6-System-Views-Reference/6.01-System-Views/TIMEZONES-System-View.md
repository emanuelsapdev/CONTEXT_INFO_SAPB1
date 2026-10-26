# 6.1.172 TIMEZONES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1602–1603

Provides information about the timezones which are available together with their originating data set.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| TIMEZONE_NAME | NVARCHAR(64) | Displays the name of the respective timezone that can be used as parameter to give the source respective destination timezone for UTCTOLOCAL and LOCALTOUTC. |
| TIMEZONE_DATASET | NVARCHAR(8) | Displays the data set in which the time zones definition is located. It can take the values sap or platform as they are allowed for the dataset parameter to UTCTOLOCAL/LOCALTOUTC. The value of this column can thus be directly used as an input for the respective UTCTOLOCAL/LOCALTOUTC parameter. |

## Related Information

ALTER SYSTEM CLEAR TIMEZONE CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-TIMEZONE-CACHE-Statement-System.md) LOCALTOUTC Function (Datetime) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LOCALTOUTC-Function-Datetime.md) UTCTOLOCAL Function (Datetime) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/UTCTOLOCAL-Function-Datetime.md) M_TIMEZONE_ALERTS System View [→](../6.02-Monitoring-Views/M_TIMEZONE_ALERTS-System-View.md)
