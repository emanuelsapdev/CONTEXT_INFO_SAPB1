# 4.10.1.25 ALTER WORKLOAD CLASS Statement (Workload Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 646–649

Changes workload classes.

## Syntax

```sql
ALTER WORKLOAD CLASS { <workload_class_name> { <property_list> | ENABLE |
DISABLE }
   | ALL { ENABLE | DISABLE } }
```

## Syntax Elements

#### workload_class_name

Changes the specified workload class.

```sql
<workload_class_name> ::= <identifier>
```

#### property_list

Defines the properties of a workload class. The properties have the format of key-value pairs.

```sql
property_list ::=
   [SET | UNSET] {'<key>' = '<value>'}[,{'<key>' = '<value>'}] [...]
```

```sql
<key> ::=
 PRIORITY
 | STATEMENT MEMORY LIMIT
 | STATEMENT THREAD LIMIT
 | STATEMENT TIMEOUT
 | TOTAL STATEMENT MEMORY LIMIT
 | TOTAL STATEMENT THREAD LIMIT
 | WRITE TRANSACTION LIFETIME
 | IDLE CURSOR LIFETIME
```

- PRIORITY is a value from 0-9. A higher number specifies a higher priority.
- STATEMENT MEMORY LIMIT specifies a limit in GB. For example, STATEMENT MEMORY LIMIT = '2' specifies a 2 GB limit.
- STATEMENT THREAD LIMIT is a statement concurrency limit, rather than a thread limit; SAP HANA does not impose a thread limit on statements.
- STATEMENT TIMEOUT specifies an expiry time for statement execution, after which statement execution is canceled and the transaction is rolled back. The default is 0 (no expiry).
- TOTAL STATEMENT MEMORY LIMIT specifies an overall total memory limit, in GB, for all statements belonging to a specific workload class. If this property is specified, then PRIORITY and TOTAL STATEMENT THREAD LIMIT must also be specified.
- TOTAL STATEMENT THREAD LIMIT specifies an overall limit for the number of active threads scheduled for statements for the specific workload class. If this property is specified, then PRIORITY and TOTAL STATEMENT MEMORY LIMIT must also be specified.
- WRITE TRANSACTION LIFETIME specifies the duration of uncommitted write transactions, in minutes, before the connection is terminated. If set to 0, then the timeout behavior is disabled.
- IDLE CURSOR LIFETIME specifies the duration of cursors, in minutes, before the connection is terminated. If set to 0, then the timeout behavior is disabled.

#### ENABLE or DISABLE

Enables or disables the workload class. **ALL** Changes all workload classes.

## Description

A workload class with only NULL values behaves like the default workload class.

An aggregated workload class must have all properties specified (TOTAL STATEMENT MEMORY LIMIT, TOTAL STATEMENT THREAD LIMIT, PRIORITY).

**Precedence in the case of competing settings**: In the case of competing settings between workload class settings and user parameter settings (set by using ALTER USER), a workload class setting takes precedence over a user parameter setting. Workload class settings and user parameter settings always take precedence over `.ini` file settings. If the STATEMENT TIMEOUT setting, which can also be set by the client, is set to something more restrictive by the client than the value that is determined after evaluating the setting on the server side, then the more restrictive client-side setting is used instead. The following table demonstrates how precedence is determined:

| **global.ini** | **User parameters** | **Workload class** | **Resulting effective values(statement execution)** |
| --- | --- | --- | --- |
| memory 50 GB | priority 5, thread 5 | if not matched class found | priority 5, thread limit 5, memory limit 50GB |
| memory 50 GB | priority 5, thread 5, memory 5 | priority 7, thread limit 10, memory limit 50GB | priority 7, thread limit 10, memory limit 50GB |
| memory 50 GB | priority 5, thread 5, memory 30GB | priority 7, thread limit 10, memory limit undefined | priority 7, thread limit 10, memory limit 30GB |
| memory 50 GB | priority 5, thread 5, memory 30GB | priority 7, total thread limit 10, total memory limit 50GB | priority 7, total thread limit 10, total memory limit 50GB |
| memory 50 GB | priority 5, thread 5, memory 30GB | priority 7, total thread limit undefined, total memory limit 50GB (SQL error returned at CREATE/ALTER WORKLOAD CLASS) | priority 5, thread limit 5, memory limit 30GB |
| memory 50 GB | priority 5, thread 5, memory 30GB | priority 7, total thread limit 10, total memory limit undefined (SQL error returned at CREATE/ALTER WORKLOAD CLASS) | priority 5, thread limit 5, memory limit 30GB |
| statement timeout 2 seconds | N/A | statement timeout 5 seconds | statement time out is 5 unless the value was set more restrictively by the client. For example, if the client-side setting is 3, then 3 becomes the effective value. |

## Examples

Unset the value for the STATEMENT_MEMORY_LIMIT for an existing workload class, MyWorkloadClass. The WORKLOAD_CLASSES view displays the value NULL for the column STATEMENT_MEMORY_LIMIT of this workload class. It also changes the PRIORITY to 5.

```sql
ALTER WORKLOAD CLASS "MyWorkloadClass"
   UNSET 'STATEMENT MEMORY LIMIT'
   SET 'PRIORITY' = '5';
```

Enable all workload classes and their related mappings.

```sql
ALTER WORKLOAD CLASS ALL ENABLE;
```

## Related Information

CREATE WORKLOAD CLASS Statement (Workload Management) [→](CREATE-WORKLOAD-CLASS-Statement-Workload-Management.md) WORKLOAD_CLASSES System View [→](../../../6-System-Views-Reference/6.01-System-Views/WORKLOAD_CLASSES-System-View.md)
