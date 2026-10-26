# 4.10.1.19.27 ALTER SYSTEM CLEAR TRACES Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 511–513

Clears (removes) trace files opened by SAP HANA.

## Syntax

```sql
ALTER SYSTEM CLEAR TRACES ( <trace_type_list> ) [ UNTIL <timestamp> ] [ WITH
BACKUP ]
```

## Syntax Elements

#### trace_type_list

Specifies a list of trace types to be cleared.

```sql
<trace_type_list> ::= <trace_type> [, <trace_type> [,…] ]
```

##### trace_type

Specifies the trace type.

```sql
<trace_type> ::= <string_literal>
```

You can selectively clear specific trace files by setting `<trace_type>` to one of the following types:

| `<trace_type>` | **Trace Files** |
| --- | --- |
| ALERT | \*alert_\*.trc |
| CLIENT | localclient_\*.trc |
| CRASHDUMP | \*.crashdump.\* |
| EMERGENCYDUMP | \*.emergencydump.\* |
| EXPENSIVESTATEMENT | \*.expensive_statements.\*.trc |
| RTEDUMP | \*.rtedump.\*.trc |
| UNLOAD | \*.unloads.\*.trc |
| ROWSTOREREORG | \*.row_store_reorg.\*.trc |
| SQLTRACE | sqltrace\*.py |
| BACKUP | backup.log |
| BACKINT | backint.log |
| \* | all \*.trc files of services listed below |
| indexserver,nameserver,...,daemon | open \*.trc files of a single service type |

#### timestamp

Specifies that all trace files with a modification time before or equal to the timestamp are deleted.

```sql
<timestamp> ::= <string_literal>
```

**WITH BACKUP** Specifies that trace files are compressed and saved instead of removed.

## Description

When you use this statement, all trace files and compressed files (like .gz) that were opened by the SAP HANA database are removed, assuming WITH BACKUP is not specified.

On distributed systems, this command clears all trace files on all hosts.

Use this command to reduce disk space used by large trace files for example, when trace components are set to INFO or DEBUG.

## Examples

Clear the alert trace file.

```sql
ALTER SYSTEM CLEAR TRACES('ALERT');
```

Clear the alert and client trace files.

```sql
ALTER SYSTEM CLEAR TRACES('ALERT', 'CLIENT');
```

Back up the alert and client trace files.

```sql
ALTER SYSTEM CLEAR TRACES('ALERT', 'CLIENT') WITH BACKUP;
```

Clear the alert and client trace files with a timestamp prior or equal to 2015-12-31 23:59:59.999.

```sql
ALTER SYSTEM CLEAR TRACES ('ALERT', 'CLIENT') UNTIL '2015-12-31 23:59:59';
```

Back up the indexserver trace files.

```sql
ALTER SYSTEM CLEAR TRACES('indexserver') WITH BACKUP;
```

## Related Information

ALTER SYSTEM REMOVE TRACES Statement (System Management) [→](ALTER-SYSTEM-REMOVE-TRACES-Statement-System-Management.md) M_TRACEFILES System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_TRACEFILES-System-View.md) ALTER SYSTEM {START | STOP} PERFTRACE Statement (System Management) [→](ALTER-SYSTEM-START-STOP-PERFTRACE-Statement-System.md) M_TRACEFILES System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_TRACEFILES-System-View.md) M_TRACEFILE_CONTENTS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_TRACEFILE_CONTENTS-System-View.md) ALTER SYSTEM CLEAR TRACES Statement (System Management) [→](ALTER-SYSTEM-CLEAR-TRACES-Statement-System-Management.md)
