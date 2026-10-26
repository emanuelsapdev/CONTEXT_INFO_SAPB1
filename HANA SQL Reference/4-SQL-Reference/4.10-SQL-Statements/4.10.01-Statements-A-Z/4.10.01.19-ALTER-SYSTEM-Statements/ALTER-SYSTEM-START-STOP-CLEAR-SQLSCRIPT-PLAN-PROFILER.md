# 4.10.1.19.55 ALTER SYSTEM {START | STOP | CLEAR} SQLSCRIPT PLAN PROFILER Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 549–550

Starts, stops, and clears the SQLScript Plan Profiling feature.

## Syntax

```sql
ALTER SYSTEM { START | STOP | CLEAR } SQLSCRIPT PLAN PROFILER [ <filter> ]
<filter> ::= FOR SESSION <session_id> | FOR PROCEDURE <procedure_name>
```

## Syntax Element

#### START

Enables the SQLScript plan profiler. **STOP** Disables the SQLScript plan profiler. **CLEAR** Clears the results of the SQLScript plan profiler from the M_SQLSCRIPT_PLAN_PROFILER_RESULTS system view.

#### filter

Specifies the scope of plan profiling - either a session, or a procedure. When a filter is applied, only the statements executed in the specified scope is profiled. The default is the entire system.

## Description

Use this statement to enable SQLScript plan profiling for a session or procedure, or to stop SQLScript plan profiling, or clear the results from profiling.

You can query SQLScript plan profiling results from the M_SQLSCRIPT_PLAN_PROFILER_RESULTS system view. To display a list of the sessions and procedures that are being profiled using the SQLScript plan profiler, query the M_SQLSCRIPT_PLAN_PROFILERS system view.

You can also enable the SQLScript plan profiler for a procedure by adding the SQLSCRIPT_PLAN_PROFILER hint to a CALL statement (for example, `CALL P1 WITH HINT(SQLSCRIPT_PLAN_PROFILER)`).

## Permissions

You must have the TRACE ADMIN or OPTIMIZER ADMIN system privilege to execute this statement.

## Example

The following example starts the SQLScript plan profiler:

```sql
ALTER SYSTEM START SQLSCRIPT PLAN PROFILER;
```

## Related Information

M_SQLSCRIPT_PLAN_PROFILER_RESULTS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SQLSCRIPT_PLAN_PROFILER_RESULTS-System-View.md) M_SQLSCRIPT_PLAN_PROFILERS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SQLSCRIPT_PLAN_PROFILERS-System-View.md)
