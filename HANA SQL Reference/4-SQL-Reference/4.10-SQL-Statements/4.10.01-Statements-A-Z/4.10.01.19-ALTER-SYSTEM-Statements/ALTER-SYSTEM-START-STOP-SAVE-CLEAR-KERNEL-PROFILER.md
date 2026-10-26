# 4.10.1.19.54 ALTER SYSTEM {START | STOP | SAVE | CLEAR} KERNEL PROFILER Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 545–549

Manages the operation of the Kernel Profiler.

## Syntax

```sql
ALTER SYSTEM { <start_profiler>
 | <stop_profiler>
 | <save_profiler>
 | <clear_profiler>
 }
```

## Syntax Element

#### start_profiler

Starts the Kernel Profiler.

```sql
<start_profiler> ::= START KERNEL PROFILER
 [ <location> ]
 [ <profile_by> ]
 [ <memory_limit> ]
 [ <sampling_interval> ]
```

##### location

Restricts profiling to the specified location. See the definition of `<location>` later in this list.

##### profile_by

Sets the scope of the profiling.

```sql
<profile_by> ::= { <user_name>
 | <application_user_name>
 | <connection_id>
 | <root_statement_hash>
 | <traceprofile_name> }
```

###### user_name

Restricts profiling to the specified SQL user name.

```sql
<user_name> ::= USER <simple_identifier>
```

###### application_user_name

Restricts profiling to the specified application user name.

```sql
<application_user_name> ::= APPLICATIONUSER <string_literal>
```

###### connection_id

Restricts profling to the specified connection ID.

```sql
<connection_id> ::= SESSION <numeric_literal>
```

###### root_statement_hash

Restricts profiling to the specified root statement hash.

```sql
<root_statement_hash> ::= ROOT_STATEMENT_HASH '<string_literal>'
```

###### traceprofile_name

Restricts profiling to the specified userspecific trace profile.

```sql
<traceprofile_name> ::= TRACEPROFILE <string_literal>
```

##### memory_limit

Sets an approximate memory limit (in bytes) for the Kernel Profiler. If not specified, the default is 0 (no limit).

```sql
<memory_limit> ::= MEMORY LIMIT <numeric_literal>
```

##### sampling_interval

Periodically stores profiler samples, according to specified interval (in milliseconds). If not specified, the default is 1 millisecond.

```sql
<sampling_interval> ::= SAMPLING INTERVAL <numeric_literal>
```

#### stop_profiler

Stops the Kernel Profiler (but does not free up the allocated memory).

```sql
<stop_profiler> ::= STOP KERNEL PROFILER [ <location> ]
```

`<location>` restricts profiling to the specified location. See the definition of `<location>` later in this topic.

#### save_profiler

Stops the Kernel Profiler, if it is running, saves the data to the trace directory, and clears the allocated memory

```sql
<save_profiler> ::= SAVE KERNEL PROFILER [ <location> ] [ <filter_list> ]
[ <into_files> ]
<filter_list> ::= FOR CALLSTACKS <string_literal> [, <string_literal>
[, ... ] ]
<into_files> ::= INTO { [ CPU FILE <file_name_cpu> ] [ WAIT FILE
<file_name_wait> ] }
<file_name_cpu> ::= <string_literal>
<file_name_wait> ::= <string_literal>
```

##### location

Restricts profiling to the specified location. See the definition of `<location>` later in this topic.

##### filter_list

Filters the profiling output to the specified call stacks.

##### into_files

Writes Kernel Profiler output to the specified file(s) in the trace directory of your SAP HANA database instance.

If the INTO clause is not specified, then the default names of files it creates are `kernel_profiler_cpu.dot` and `kernel_profiler_wait.dot`. However, if only one file type is specified, only this file is created (the other file is not created with its default file name).

You cannot specify a path for the files. Also, files of the same name are overwritten.

#### clear_profiler

Stops the Kernel Profiler, and clears the allocated memory.

```sql
<clear_profiler> ::= CLEAR KERNEL PROFILER [ <location> ]
```

`<location>` restricts profiling to the specified location. See the definition of `<location>` later in this topic.

#### location

Restricts the Kernel Profiler to the specified location.

```sql
<location> ::= AT [ LOCATION ] <host_and_port>
<host_and_port> ::= { ( <host> , <port> ) | '<host>:<port>' }
<host> ::= <string_literal>
<port> ::= <numeric_literal>
```

## Description

The Kernel Profiler is a tool which collects information about CPU consumption and wait times for SAP HANA's various internal processes. This information can be helpful in support scenarios.

Only one instance of the Kernel Profiler can be active at a time using the ALTER SYSTEM statement, which can be monitored with the M_KERNEL_PROFILER system view.

## Permissions

You must have the RESOURCE ADMIN or TRACE ADMIN system privilege to execute this statement.

## Examples

The following statement clears all previously collected Kernel Profiler data.

```sql
ALTER SYSTEM CLEAR KERNEL PROFILER;
```

The following statement starts profiling for the SYSTEM user, sets a memory limit of 1 GB, and sets a sampling interval of 2 milliseconds.

```sql
ALTER SYSTEM START KERNEL PROFILER USER SYSTEM MEMORY LIMIT 1073741824 SAMPLING
INTERVAL 2;
```

The following statement stops profiling, saves the data for the specified call stacks into the trace directory, and then frees the memory that was used for the profiling data.

```sql
ALTER SYSTEM SAVE KERNEL PROFILER FOR CALLSTACK
'Execution::JobExecWatchdog::run','System::ProcessorInfo::getCurrentProcessorInde
x' INTO CPU FILE 'cpu.dot' WAIT FILE 'wait.dot';
```

The following statement starts profiling at host:port `ab1234:30003` and filters for the userspecific trace (database trace) profile `MYTRACEPROFILE`.

```sql
ALTER SYSTEM START KERNEL PROFILER AT 'ab1234:30003' TRACEPROFILE
'MYTRACEPROFILE';
```

The following statement stops profiling and clears the profiling data for the specified location `ab1234:30003`. In this case, because the Kernel Profiler is being stopped, and the data cleared, no data will be saved.

```sql
ALTER SYSTEM CLEAR KERNEL PROFILER AT LOCATION 'ab1234:30003';
```

The following example shows how to profile using the root statement hash:

```sql
ALTER SYSTEM START KERNEL PROFILER ROOT_STATEMENT_HASH
'a68e7882f87a2ec501604ce6feb7dee7';
 SELECT TOP 10 * from M_SERVICE_THREADS ORDER BY DURATION;         --has this
hash (maybe execute several times)
 ALTER SYSTEM STOP KERNEL PROFILER;
 SELECT * FROM SYS.M_KERNEL_PROFILER;                               --check for
root_statement_hash column and also if SAMPLE_COUNT > 0
 ALTER SYSTEM SAVE KERNEL PROFILER;                                 --if
SAMPLE_COUNT > 0
 ALTER SYSTEM CLEAR KERNEL PROFILER;
```

## Related Information

[M_KERNEL_PROFILER System View](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_KERNEL_PROFILER-System-View.md)
