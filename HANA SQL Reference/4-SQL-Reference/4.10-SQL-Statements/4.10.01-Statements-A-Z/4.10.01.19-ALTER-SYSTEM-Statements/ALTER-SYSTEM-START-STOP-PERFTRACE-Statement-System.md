# 4.10.1.19.58 ALTER SYSTEM {START | STOP} PERFTRACE Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 553–555

Starts or stops performance tracing.

> **Note**
>
> Performance tracing is only to be used in conjunction with SAP Support personnel. The collected performance trace data cannot be analyzed by an end user.

## Syntax

```sql
ALTER SYSTEM START PERFTRACE [ <user_name> ] [ <application_user_name> ]
   [ <application_name> ] [ <passport_level> ]
   [ PLAN_EXECUTION ] [ FUNCTION_PROFILER ] [ DURATION <duration_seconds> ]
   [ <root_statement_hash> ]
| ALTER SYSTEM STOP PERFTRACE
```

## Syntax Element

#### user_name

Restricts performance trace collection to an SQL user name.

```sql
<user_name> ::= USER <simple_identifier>
```

#### application_user_name

Restricts performance trace collection to the application user name.

```sql
<application_user_name> ::= APPLICATIONUSER <string_literal>
```

#### application_name

Restricts performance trace collection to the application name.

```sql
<application_name> ::= APPLICATION <string_literal>
```

#### passport_level

Specifies the level of trace data to be collected.

```sql
<passport_level> ::= PASSPORT_TRACELEVEL { MEDIUM | HIGH }
```

`<passport_level>` filters the amount of data collected in end-to-end scenarios.

#### PLAN_EXECUTION

Specifies that plan execution details should be traced.

#### FUNCTION_PROFILER

Specifies that function-level details should be traced.

#### duration_seconds

Specifies the number of seconds to run the performance trace for. If not specified, the trace runs until the ALTER SYSTEM STOP PERFTRACE statement is executed.

```sql
<duration_seconds> ::= <numeric_literal>
```

After this period expires, the performance trace is automatically stopped. If you do not specify this parameter, then you must stop the performance trace with the ALTER SYSTEM STOP PERFTRACE statement.

#### root_statement_hash

Restricts performance trace collection to the statement identified by the root statement hash.

```sql
<root_statement_hash> ::= ROOT_STATEMENT_HASH <string_literal>
```

For statements in stored procedures, the root statement hash is the statement hash of the stored procedure call. The perftrace filter compares the given root statement hash with the root statement hash of the statements. This will also trace statements running within a stored procedure.

## Description

Only one performance trace can be active at a time.

After stopping the trace, collect and save the performance trace data with the ALTER SYSTEM SAVE PERFTRACE statement.

## Example

Start performance tracing for the user sql_user on application user name app_user for application app_name, and specify that plan execution and function-level detail should be traced.

```sql
ALTER SYSTEM START PERFTRACE USER sql_user APPLICATIONUSER app_user APPLICATION
app_name PLAN_EXECUTION FUNCTION_PROFILER;
```

Start performance tracing that is filtered by the statement hash 21db1b17968de7861e6c97645f72963b.

```sql
ALTER SYSTEM START PERFTRACE ROOT_STATEMENT_HASH
'21db1b17968de7861e6c97645f72963b';
```

Stop an active performance trace.

```sql
ALTER SYSTEM STOP PERFTRACE;
```

## Related Information

ALTER SYSTEM SAVE PERFTRACE Statement (System Management) [→](ALTER-SYSTEM-SAVE-PERFTRACE-Statement-System-Management.md) M_PERFTRACE System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_PERFTRACE-System-View.md) ALTER SYSTEM CLEAR TRACES Statement (System Management) [→](ALTER-SYSTEM-CLEAR-TRACES-Statement-System-Management.md) ALTER SYSTEM REMOVE TRACES Statement (System Management) [→](ALTER-SYSTEM-REMOVE-TRACES-Statement-System-Management.md) ALTER SYSTEM {START | STOP} PERFTRACE Statement (System Management) [→](ALTER-SYSTEM-START-STOP-PERFTRACE-Statement-System.md) M_TRACEFILE_CONTENTS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_TRACEFILE_CONTENTS-System-View.md) M_TRACE_CONFIGURATION System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_TRACE_CONFIGURATION-System-View.md)
