# 6.1.194 WORKLOAD_MAPPINGS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1629–1631

Provides information about available workload mappings.

| **Column Name** | **Data Type** | **Description** |
| --- | --- | --- |
| WORKLOAD_MAPPING_NAME | NVARCHAR(256) | Dislays the workload mapping name. |
| WORKLOAD_CLASS_NAME | NVARCHAR(256) | Dislays the workload class name. |
| USER_NAME | NVARCHAR(256) | Dislays the user name. |
| USERGROUP_NAME | NVARCHAR(256) | Dislays the name of the user group. |
| APPLICATION_USER_NAME | NVARCHAR(256) | Dislays the session variable APPLICA TIONUSER. |
| APPLICATION_USER_NAME_WILDCARD | NVARCHAR(1) | Dislays the wildcard character that is allowed in the user name. |
| APPLICATION_NAME | NVARCHAR(256) | Dislays the session variable APPLICA TION. |
| APPLICATION_NAME_WILDCARD | NVARCHAR(1) | Dislays the wildcard character that is used in APPLICATION_NAME. |
| APPLICATION_TENANT_NAME | NVARCHAR(64) | Displays the session variable of the application tenant. |
| APPLICATION_TENANT_NAME_WILDCARD | NVARCHAR(1) | Displays the wild card of the application tenant. |
| CLIENT | NVARCHAR(3) | Dislays the session variable CLIENT. |
| CLIENT_WILDCARD | NVARCHAR(1) | Dislays the wildcard character tha tis used in CLIENT. |
| APPLICATION_COMPONENT_NAME | NVARCHAR(256) | Dislays the name of the application component. |
| APPLICATION_COMPONENT_NAME_WILDCARD | NVARCHAR(1) | Dislays the wildcard character that is used in APPLICATION_COMPONENT_NAME. |
| APPLICATION_COMPONENT_TYPE | NVARCHAR(256) | Dislays the type of application component. |
| APPLICATION_COMPONENT_TYPE_WILDCARD | NVARCHAR(1) | Dislays the wildcard character that is used in APPLICATION_COMPONENT_TYPE. |
| SCHEMA_NAME | NVARCHAR(256) | Dislays the name of the schema. |
| OBJECT_NAME | NVARCHAR(256) | Dislays the name of the object. |
| IS_ENABLED | NVARCHAR(5) | Dislays the workload class is enabled: TRUE/FALSE. |
| XS_APPLICATION_USER_NAME | NVARCHAR(256) | Dislays the user name assigned to the session variable XS_APPLICATIONUSER. |
| XS_APPLICATION_USER_NAME_WILDCARD | NVARCHAR(1) | Dislays the wildcard character that is used for the session variable XS_APPLICATIONUSER. |

## Related Information

CREATE WORKLOAD MAPPING Statement (Workload Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-WORKLOAD-MAPPING-Statement-Workload-Management.md) ALTER WORKLOAD MAPPING Statement (Workload Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-WORKLOAD-MAPPING-Statement-Workload-Management.md) DROP WORKLOAD MAPPING Statement (Workload Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-WORKLOAD-MAPPING-Statement-Workload-Management.md) M_WORKLOAD System View [→](../6.02-Monitoring-Views/M_WORKLOAD-System-View.md) WORKLOAD_CLASSES System View [→](WORKLOAD_CLASSES-System-View.md)
