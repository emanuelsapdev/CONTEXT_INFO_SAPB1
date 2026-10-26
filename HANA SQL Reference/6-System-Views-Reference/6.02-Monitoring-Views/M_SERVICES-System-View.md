# 6.2.252 M_SERVICES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1987–1988

Provides the status of all services.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SERVICE_NAME | VARCHAR(32) | Displays the service name. See M_SERVICE_TYPES for all known service names. |
| PROCESS_ID | INTEGER | Displays the process ID. |
| DETAIL | VARCHAR(128) | Internal use only. Use COORDINATOR_TYPE to test the service role. |
| ACTIVE_STATUS | VARCHAR(16) | Displays the active status: NO, YES, UNKNOWN, STARTING, or STOPPING. |
| SQL_PORT | INTEGER | Displays the SQL port. |
| COORDINATOR_TYPE | VARCHAR(16) | Displays the coordinator type in the distributed landscape: MASTER, SLAVE, STANDBY, or NONE. |
| IS_DATABASE_LOCAL | VARCHAR(2) | Displays whether or not the service is local to the database, tenant, or if it belongs to one specific database. |

## Related Information

ALTER SYSTEM STOP SERVICE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-STOP-SERVICE-Statement-System-Management.md) ALTER SYSTEM RECONFIGURE SERVICE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RECONFIGURE-SERVICE-Statement-System-Management.md) M_SERVICE_TYPES System View [→](M_SERVICE_TYPES-System-View.md)
