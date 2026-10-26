# 4.10.1.19.49 ALTER SYSTEM REMOVE TRACES Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 539–540

Deletes the trace files on a specified host to reduce the disk space used by large trace files.

## Syntax

```sql
ALTER SYSTEM REMOVE TRACES (<hostname>, <trace_file_list>)
```

## Syntax Elements

#### hostname

Specifies the name of the host where the traces are to be removed.

```sql
<hostname> ::= <string_literal>
```

#### trace_file_list

Specifies the trace files to be removed.

```sql
<trace_file_list> ::=
 <trace_file> [{, <trace_file>}...]
```

`<trace_file>` specifies the name of a file to be removed.

## Description

Valid host name and file name combinations can be retrieved from the M_TRACEFILES system view.

When a service has a trace file open, it cannot be deleted. In this case, clear the trace file by using the ALTER SYSTEM CLEAR TRACES statement.

## Example

This command deletes files on the host named HOST_NAME.

```sql
ALTER SYSTEM REMOVE TRACES ('hananode01', 'extrace.py', 'extrace.py.old');
```

## Related Information

M_TRACEFILES System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_TRACEFILES-System-View.md) ALTER SYSTEM CLEAR TRACES Statement (System Management) [→](ALTER-SYSTEM-CLEAR-TRACES-Statement-System-Management.md) ALTER SYSTEM {START | STOP} PERFTRACE Statement (System Management) [→](ALTER-SYSTEM-START-STOP-PERFTRACE-Statement-System.md)
