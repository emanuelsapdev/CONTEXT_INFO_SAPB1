# 6.2.299 M_SYSTEM_REPLICATION System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2065–2068

Monitors system replication information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SITE_ID | INTEGER | Displays the generated site ID. |
| SITE_NAME | VARCHAR(256) | Displays the site name. |
| SECONDARY_SITE_ID | INTEGER | Displays the generated site ID of the secondary site. |
| SECONDARY_SITE_NAME | VARCHAR(256) | Displays the secondary logical site name. |
| REPLICATION_MODE | VARCHAR(7) | Displays the configured replication mode:<br>• SYNC: the synchronous replication that acknowledges when a buffer has been written to a disk.<br>• SYNCMEM: the synchronous replication that acknowledges when a buffer has arrived in the memory.<br>• ASYNC: the asynchronous replication.<br>• UNKNOWN: set if the replication mode cannot be determined (for example, if there is a communication error when getting status information from a service). |
| REPLICATION_STATUS | VARCHAR(12) | Displays the replication status. |
| OPERATION_MODE | VARCHAR(32) | Displays the operation mode. |
| SECONDARY_READ_ACCESS_STATUS | VARCHAR(16) | Indicates whether the secondary system is read-enabled and if read access is activated:<br>• NOT CONFIGURED: Displays that an operation mode is used that does not allow read access.<br>• STOPPED: Displays that the secondary is running in operation mode logreplay_readaccess, but it is currently stopped.<br>• VERSION MISMATCH: Displays that the secondary system is running in operation mode logre play_readaccess but read access is internally disabled on the secondary system because it is on a different SAP HANA version than the primary system.<br>• INITIALIZING: Displays that the secondary site is running in operation mode logreplay_readaccess but read access is not yet completely initialized. SQL connections to the secondary system fail in this state.<br>• CONSISTENT: Displays that log replay on the secondary site has reached a global consistent state, but the SQL port is not open.<br>• ACTIVE: Displays that the secondary system is running in operation mode logreplay_readaccess and is initialized for read access. SQL connections are possible in this state. |
| TIER | INTEGER | Displays the tier on which the source site is located. |

## Related Information

ALTER SYSTEM {REGISTER | UNREGISTER} SYSTEM REPLICATION SITE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REGISTER-UNREGISTER-SYSTEM-REPLICATION-SITE.md) ALTER SYSTEM {ENABLE | DISABLE} SYSTEM REPLICATION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ENABLE-DISABLE-SYSTEM-REPLICATION-Statement.md)
