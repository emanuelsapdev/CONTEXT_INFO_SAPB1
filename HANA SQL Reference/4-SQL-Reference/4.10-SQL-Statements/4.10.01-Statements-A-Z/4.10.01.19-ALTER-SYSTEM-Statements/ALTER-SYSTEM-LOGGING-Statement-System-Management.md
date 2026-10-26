# 4.10.1.19.34 ALTER SYSTEM LOGGING Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 522–523

Enables or disables logging.

## Syntax

```sql
ALTER SYSTEM LOGGING <on_off>
```

## Syntax Elements

#### on_off

Specifies the logging status.

```sql
<on_off> ::= ON | OFF
```

##### ON

Enables logging.

##### OFF

Disables logging.

## Description

While logging is disabled, no log entries persist; only the data area is written when a savepoint is reached. This behavior can cause the loss of committed transactions when the indexserver terminates in the middle of a LOAD operation. In case of a termination, truncate and insert all data again.

> **Note**
>
> Logging mode cannot be disabled on the primary system when system replication is used.

After enabling logging, perform a savepoint to be sure that all data persists. You must also perform a data backup; otherwise, you are unable to recover this data.

ALTER SYSTEM LOGGING waits for the end (commit/rollback) of existing active write transactions. During the execution of this command, write transactions are blocked. In the event that there is a long-running write transaction, this command can fail with a lock wait timeout error. Starting a new write transaction also can be blocked and failed with the same error.

Only use this command while performing the initial load of a database. If this statement is used at other times, then data loss can occur if the indexserver is terminated while logging is disabled. Consequently, in a running system, the logging mode should be always ON and should not be modified.

## Example

Disable system logging.

```sql
ALTER SYSTEM LOGGING OFF;
```

Enable system logging.

```sql
ALTER SYSTEM LOGGING ON;
```

## Related Information

[ALTER TABLE Statement (Data Definition)](../4.10.01.20-ALTER-TABLE/README.md)
