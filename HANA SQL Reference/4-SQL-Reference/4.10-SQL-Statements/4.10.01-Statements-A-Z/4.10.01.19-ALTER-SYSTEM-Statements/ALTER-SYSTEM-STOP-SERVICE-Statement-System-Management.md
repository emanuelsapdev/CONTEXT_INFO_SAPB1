# 4.10.1.19.62 ALTER SYSTEM STOP SERVICE Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 560–561

Stops single or multiple services on the designated host.

## Syntax

```sql
ALTER SYSTEM STOP SERVICE <host_port> [IMMEDIATE [WITH COREFILE]]
```

## Syntax Element

#### host_port

Specifies the host and port of the service to be stopped.

```sql
<host_port> ::=
 <hostname>:<port_number> | ('<host_name>',<port_number>)
```

#### IMMEDIATE

Immediately stops the service without waiting for regular shutdown.

#### WITH COREFILE

Writes a core dump file.

## Description

Typically a service you stop is automatically restarted by the SAP HANA database system.

You should use this command after changing a configuration parameter, which requires a restart of the service.

## Example

Stop a service running on host hdb1.yourcompany.com on port 30303.

```sql
ALTER SYSTEM STOP SERVICE 'hdb1.yourcompany.com:30303';
```
