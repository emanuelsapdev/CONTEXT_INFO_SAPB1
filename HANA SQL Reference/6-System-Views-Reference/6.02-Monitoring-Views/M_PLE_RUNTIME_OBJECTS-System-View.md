# 6.2.208 M_PLE_RUNTIME_OBJECTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1934–1935

Lists all the internal cache objects created to support the planning sessions, with details about each one.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| OBJECT_TYPE | VARCHAR(32) | Displays the object type:<br>• LOOKUP DICTIONARY<br>• TIMETABLE DICTIONARY<br>• FISCPERTABLE DICTIONARY<br>• CONVERSTION DICTIONARY<br>• FOX REFERENCE DATA DICTION ARY |
| OBJECT_SCOPE | VARCHAR(45) | Displays the object scope: SESSION/ GLOBAL. |
| OBJECT_NAME | NVARCHAR(5000) | Displays the object name. This name is a generated, unique name for the run time object, derived from the corresponding session group name, session name, planning command name, and source columns. |
| CREATE_TIME | TIMESTAMP | Displays the creation time. |
| SOURCE_COLUMNS | NVARCHAR(2000) | Displays the source columns. |
| MEMORY_SIZE | BIGINT | Displays the memory size, in bytes. |
| ENTRY_COUNT | BIGINT | Displays the number of entries in the runtime object. |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SITE_ID | INTEGER | Displays the site ID of the secondary site. This value is -1 on a single instance. |

## Related Information

M_PLE_SESSIONS System View [→](M_PLE_SESSIONS-System-View.md) Session Variables [→](../../4-SQL-Reference/4.08-Session-Variables.md)
