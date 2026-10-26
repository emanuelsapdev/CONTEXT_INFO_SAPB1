# 4.10.1.19.44 ALTER SYSTEM RECONFIGURE SERVICE Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 533–534

Reconfigures a specified service by applying the current configuration parameters.

## Syntax

```sql
ALTER SYSTEM RECONFIGURE SERVICE (<service_name>,<hostname>,<port_number>)
```

## Syntax Element

#### service_name

Specifies the name of the service you wish to reconfigure. See the M_SERVICE_TYPES monitoring view topic for a list of available service types.

```sql
<service_name> ::= <string_literal>
```

#### hostname

Specifies the hostname and port number where you would like to reconfigure a service.

```sql
<hostname> ::= <string_literal>
<port_number> ::= <unsigned_integer>
```

## Description

You use ALTER SYSTEM RECONFIGURE SERVICE to reconfigure a specified service by applying the current configuration parameters. This command is used after changing multiple configuration parameters with the ALTER CONFIGURATION command without the RECONFIGURE option set. See the ALTER SYSTEM ALTER CONFIGURATION topic.

To reconfigure a specific service specify `<hostname>` and `<port_number>` and leave `<service_name>` empty. To reconfigure all services of a type, specify `<service_name>` and leave `<hostname>` and `<port_number>` empty. To reconfigure all services, leave all parameters empty.

## Example

You use the following command to reconfigure all services on the hana.yourcompany.com host using port number 30303:

```sql
ALTER SYSTEM RECONFIGURE SERVICE ('','hana.yourcompany.com',30303);
```

You use the following command to reconfigure all services of type indexserver:

```sql
ALTER SYSTEM RECONFIGURE SERVICE ('indexserver','',0);
```

## Related Information

ALTER WORKLOAD CLASS Statement (Workload Management) [→](../ALTER-WORKLOAD-CLASS-Statement-Workload-Management.md) ALTER SYSTEM ALTER CONFIGURATION Statement (System Management) [→](ALTER-SYSTEM-ALTER-CONFIGURATION-Statement-System-Management.md)
