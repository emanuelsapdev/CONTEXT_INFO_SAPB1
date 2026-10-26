# 6.2.246 M_SAVEPOINT_STATISTICS_RESET System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1982

Provides the savepoint statistics since the last reset.

This view contains values accumulated since the last reset of the main view M_SAVEPOINT_STATISTICS. Refer to M_SAVEPOINT_STATISTICS for information about the structure and use of this view.

This view is associated with the ALTER SYSTEM SAVEPOINT statement.

In addition to the members mentioned in M_SAVEPOINT_STATISTICS, this view also contains a timestamp field, RESET_TIME, which indicates the last time the data was reset.

## Related Information

M_SAVEPOINT_STATISTICS System View [→](M_SAVEPOINT_STATISTICS-System-View.md) ALTER SYSTEM SAVEPOINT Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-SAVEPOINT-Statement-System-Management.md)
