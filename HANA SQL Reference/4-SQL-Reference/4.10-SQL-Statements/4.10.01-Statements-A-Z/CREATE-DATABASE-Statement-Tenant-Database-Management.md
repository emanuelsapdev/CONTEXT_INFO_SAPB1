# 4.10.1.48 CREATE DATABASE Statement (Tenant Database Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 706–708

Creates a tenant database.

## Syntax

```sql
CREATE DATABASE <database_name>  [ AT [ LOCATION ] '<hostname>[:<port_number> ]
' ]
 [ ADD '<servicetype>' [ AT [ LOCATION ] '<hostname>[:<port_number> ] ' ] ]
 { AS REPLICA OF [ <source_database_name> ] AT [ LOCATION ]
'<hostname>[:<port_number> ]'
   | [ KEY MANAGEMENT CONFIGURATION <configuration_id> ]
   | SYSTEM USER PASSWORD <password> }
 [ OS USER '<username>' OS GROUP '<groupname>' ]
 [ NO START ]
 [ <restart_mode> RESTART ]
```

## Syntax Elements

#### database_name

Specifies a unique name for the tenant database.

```sql
<database_name> ::= <identifier>
```

#### hostname

Specifies the name of the host to create the tenant database on.

#### port_number

Specifies the port number for the host.

#### ADD servicetype

Specifies a service type for the tenant database.

```sql
<servicetype> ::= <identifier>
```

#### AS REPLICA OF [source_database_name]

Specifies the unique name of the source database to be replicated.

```sql
<source_database_name> ::= <identifier>
```

#### KEY MANAGEMENT CONFIGURATION configuration_id

Specifies the key management configuration, not the user ID to use on the target system. The configuration ID must exist on the source system and is only necessary if the source system uses local secure store (LSS) with an active key management system (KMS). The user id specified within the configuration must have been granted the ENCRYPTION ROOT KEY ADMIN system privilege. The `<configuration_id>` can be obtained from the key_management_configuration view if you have the ENCRYPTION ROOT KEY ADMIN system privileges. For more information, see Create a Key Management Configuration in the SAP HANA Administration Guide for SAP HANA Platform.

#### SYSTEM USER PASSWORD password

Specifies a password for the tenant database.

#### OS USER username

The operating system user under which the tenant is executed.

```sql
<username> ::= <identifier>
```

The user must exist already. If this value is not specified, then the `sidadm` user is used.

#### OS GROUP groupname

Specifies the operating system group under which the tenant is executed.

```sql
<groupname> ::= <identifier>
```

The group must exist already. If this value is not specified, then the `sapsys` user is used.

#### restart_mode RESTART

Specifies the restart mode for the tenant database after a system restart.

```sql
<restart_mode> RESTART
<restart_mode> ::= DEFAULT | NO
```

DEFAULT RESTART restores the previous state of the tenant database before the system restart. For example, if the tenant database was not started before the system restart, then it is not started after the system restart. This is the default behavior.

NO RESTART specifies to not restart the tenant database after a system restart.

## Description

You can create multiple databases.

With the AS REPLICA OF clause, you can create the tenant database as a replica of an existing tenant database.

## Permissions

The use of this statement requires the DATABASE ADMIN privilege.

## Example

Create a tenant database with automatic host placement and automatic port assignment.

```sql
CREATE DATABASE DB0 SYSTEM USER PASSWORD Manager1;
```

Create a tenant database on a specific host accessible via a specific SQL port (30148). The SQL port number is the internal communication port number plus 1.

```sql
CREATE DATABASE DB1 AT LOCATION 'HOST_A:30147' SYSTEM USER PASSWORD Manager1;
```

Create a tenant database on a specific host, adding an additional slave index server on a specific second host and an auxiliary script server on an automatically selected host.

```sql
CREATE DATABASE DB2 AT LOCATION 'HOST_A' ADD 'indexserver' AT 'HOST_B' ADD
'scriptserver' SYSTEM USER PASSWORD Manager1;
```

## Related Information

[System Limitations](../../4.11-System-Limitations.md)
