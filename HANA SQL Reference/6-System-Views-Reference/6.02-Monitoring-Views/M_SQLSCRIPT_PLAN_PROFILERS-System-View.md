# 6.2.271 M_SQLSCRIPT_PLAN_PROFILERS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2012–2014

Lists the sessions and procedures that are currently being profiled by the SQLScript plan profiler.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USER_NAME | NVARCHAR(256) | Displays the user name. |
| START_TIME | TIMESTAMP | Displays the timestamp that the ALTER SYSTEM ... SQLSCRIPT PLAN PRO FILER statement was executed.Displays the ID of the user who executed the AL TER SYSTEM ... SQLSCRIPT PLAN PROFILER statement |
| PROCEDURE_CONNECTION_ID | BIGINT | Displays the connection ID if a FOR SESSION filter is specified, otherwise NULL. |
| PROCEDURE_SCHEMA_NAME | NVARCHAR(256) | Displays the procedure schema name if a FOR PROCEDURE filter is specified, otherwise, NULL. |
| PROCEDURE_NAME | NVARCHAR(256) | Displays the procedure name if a FOR PROCEDURE filter is specified. |
| HOST | VARCHAR(64) | Displays the host name where profiler is executed. |
| PORT | INTEGER | Displays the internal port where profiler is executed. |

## Additional Information

Displays the ID of the user who executed the ALTER SYSTEM command. Below are some examples of how this view can be used, and the values it returns based on whether profiling is enabled:

```sql
ALTER SYSTEM START SQLSCRIPT PLAN PROFILER FOR SESSION 123456;
SELECT * FROM M_SQLSCRIPT_PLAN_PROFILERS; → Returns a result like: <user>;
<time>; 123456; null(?); null(?);
ALTER SYSTEM STOP SQLSCRIPT PLAN PROFILER FOR SESSION 123456;
SELECT * FROM M_SQLSCRIPT_PLAN_PROFILERS; → Returns an empty result because
there is no active profiler for the session
ALTER SYSTEM START SQLSCRIPT PLAN PROFILER FOR PROCEDURE S1.P1;
SELECT * FROM M_SQLSCRIPT_PLAN_PROFILERS; → Returns a result like: <user>;
<time>; null(?); S1; P1;
ALTER SYSTEM STOP SQLSCRIPT PLAN PROFILER;
SELECT * FROM M_SQLSCRIPT_PLAN_PROFILERS; → Returns an empty result because
there is no active profiler.
```

## Permissions

To see all entries in the M_SQLSCRIPT_PLAN_PROFILERS system view, you must have the CATALOG READ or OPTIMIZER ADMIN system privilege.

## Related Information

ALTER SYSTEM {START | STOP | CLEAR} SQLSCRIPT PLAN PROFILER Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-START-STOP-CLEAR-SQLSCRIPT-PLAN-PROFILER.md) M_SQLSCRIPT_PLAN_PROFILER_RESULTS System View [→](M_SQLSCRIPT_PLAN_PROFILER_RESULTS-System-View.md)
