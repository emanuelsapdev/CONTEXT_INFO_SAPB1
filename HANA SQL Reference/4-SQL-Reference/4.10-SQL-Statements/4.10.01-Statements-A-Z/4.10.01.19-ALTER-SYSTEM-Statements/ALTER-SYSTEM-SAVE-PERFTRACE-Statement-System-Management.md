# 4.10.1.19.51 ALTER SYSTEM SAVE PERFTRACE Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 541–542

Collects raw performance trace data from `.prf` files and saves the information into a single `.tpt` file.

> **Note**
>
> Performance tracing is only to be used in conjunction with SAP Support personnel. The collected performance trace data cannot be analyzed by an end user.

## Syntax

```sql
ALTER SYSTEM SAVE PERFTRACE [INTO FILE <file_name>]
```

## Syntax Elements

#### INTO FILE file_name

Specifies the file where raw performance data is saved.

```sql
<file_name> ::= <string_literal>
```

## Description

The `.tpt` file is saved in the trace directory of your SAP HANA database instance. If you do not specify a file name, then `perftrace.tpt` is used.

Use the M_JOB_PROGRESS system view to monitor the saving of a trace file. The save job is shown as Save PerfTrace in the system view.

Saving a performance trace can take some time. You can cancel the job shown in M_JOB_PROGRESS system view by using the ALTER SYSTEM CANCEL [WORK IN] SESSION statement.

## Example

Save raw performance trace data into the `mytrace.tpt` file.

```sql
ALTER SYSTEM SAVE PERFTRACE INTO FILE 'mytrace.tpt';
```

## Related Information

ALTER SYSTEM {START | STOP} PERFTRACE Statement (System Management) [→](ALTER-SYSTEM-START-STOP-PERFTRACE-Statement-System.md) M_PERFTRACE System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_PERFTRACE-System-View.md) M_JOB_PROGRESS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_JOB_PROGRESS-System-View.md) ALTER SYSTEM LOAD PERFTRACE Statement (System Management) [→](ALTER-SYSTEM-LOAD-PERFTRACE-Statement-System-Management.md) M_PERFTRACE System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_PERFTRACE-System-View.md) M_JOB_PROGRESS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_JOB_PROGRESS-System-View.md) ALTER SYSTEM CANCEL [WORK IN] SESSION Statement (System Management) [→](ALTER-SYSTEM-CANCEL-WORK-IN-SESSION-Statement-System.md)
