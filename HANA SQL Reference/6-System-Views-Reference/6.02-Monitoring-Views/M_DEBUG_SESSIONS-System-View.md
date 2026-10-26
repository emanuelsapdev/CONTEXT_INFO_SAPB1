# 6.2.84 M_DEBUG_SESSIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1754–1755

Provides an overview of debug sessions and their properties.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| DEBUG_SESSION_ID | VARCHAR(32) | Displays the landscape-wide unique identifier for debug session. |
| COMPILE_MODE | VARCHAR(20) | Displays the compilation handling of nested procedures. |
| TIMEOUT | INTEGER | Displays the time in seconds after which the debug session will timeout and destroy itself. |
| ATTACH_COUNT | INTEGER | Displays the number of debuggees the debugger is currently attached to. |
| ATTACH_FILTER_CONNECTION_ID | INTEGER | Displays the connection ID the debugger is using to attach to connections. |
| ATTACH_FILTER_USER_NAME | NVARCHAR(256) | Displays the connection user name the debugger is using to attach to connections. |
| ATTACH_FILTER_APPLICATION_USER_NAME | NVARCHAR(256) | Displays the application user name the debugger is using to attach to connections. |
| ATTACH_FILTER_DEBUG_TOKEN | VARCHAR(32) | Displays the debug token the debugger is using to attach to connections. |

## Related Information

[M_DEBUG_CONNECTIONS System View](M_DEBUG_CONNECTIONS-System-View.md)
