# 6.2.335 M_TRACEFILES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2112–2113

Provides information about all trace files.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| FILE_NAME | VARCHAR(256) | Displays the file name. |
| FILE_SIZE | BIGINT | Displays the file size in bytes. |
| FILE_MTIME | TIMESTAMP | Displays the file date. |

## Additional Information

With the CLEAR command, all files that were opened by a service are removed or reset to size 0. On a distributed system, this command clears all traces on all hosts. .

```sql
ALTER SYSTEM CLEAR TRACES
('ALERT','CLIENT','CRASHDUMP,'*','INDEXSERVER',...,,'DAEMON' );
```

It can clear different types of files:

| **Name.** | **Files.** |
| --- | --- |
| ALERT. | \<service>alert....trc. |
| CLIENT. | localclient_....trc. |
| CRASHDUMP. | \*.crashdump....trc. |
| \*. | open \*.trc files of all active services. |
| INDEXSERVER,NAMESERVER,...,DAEMON | open \*.trc files of a single service type. |

## Related Information

M_TRACEFILE_CONTENTS System View [→](M_TRACEFILE_CONTENTS-System-View.md) ALTER SYSTEM REMOVE TRACES Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REMOVE-TRACES-Statement-System-Management.md)

ALTER SYSTEM CLEAR TRACES Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-TRACES-Statement-System-Management.md) M_SERVICE_TRACES System View [→](M_SERVICE_TRACES-System-View.md)
