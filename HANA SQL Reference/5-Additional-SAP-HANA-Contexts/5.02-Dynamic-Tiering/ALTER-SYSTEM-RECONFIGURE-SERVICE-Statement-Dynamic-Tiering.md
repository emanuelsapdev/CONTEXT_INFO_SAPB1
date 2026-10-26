# 5.2.8 ALTER SYSTEM RECONFIGURE SERVICE Statement [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1242–1244

Reconfigure a specified service by applying the current configuration parameters.

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

#### hostname,port_number

The hostname and port number where you would like to reconfigure a service.

```sql
<hostname> ::= <string_literal>
```

```sql
<port_number> ::= <unsigned_integer>
```

## Permissions

You must have the EXTENDED STORAGE ADMIN and SERVICE ADMIN system privileges.

## Description

You use ALTER SYSTEM RECONFIGURE SERVICE to reconfigure a specified service by applying the current configuration parameters. This command is used after changing multiple configuration parameters with the ALTER CONFIGURATION command without the RECONFIGURE option set. See the ALTER SYSTEM ALTER CONFIGURATION topic.

To reconfigure a specific service specify `<hostname>` and `<port_number>` and leave `<service_name>` empty. To reconfigure all services of a type, specify `<service_name>` and leave `<hostname>` and `<port_number>` empty. To reconfigure all services, leave all parameters empty.

## Example

You use the following command to reconfigure all services on the hana.yourcompany.com host using port number 30303:

```sql
ALTER SYSTEM RECONFIGURE SERVICE ('','hana.yourcompany.com',30303)
```

You use the following command to reconfigure all services of type indexserver:

```sql
ALTER SYSTEM RECONFIGURE SERVICE ('indexserver','',0)
```

## See Also

ALTER SYSTEM ALTER CONFIGURATION Statement [Dynamic Tiering] [→](5.02.07-ALTER-SYSTEM-ALTER-CONFIGURATION-DT/README.md)
