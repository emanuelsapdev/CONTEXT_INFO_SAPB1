# 4.10.1.5 ALTER DATABASE Statement (Tenant Database Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 424–428

Makes changes to a tenant database.

## Syntax

```sql
ALTER DATABASE <database_name>
 <alter_service_spec_list>
 | ALTER <service_type> AT [ LOCATION ] '<hostname>[:<port_number>]' TO
[ LOCATION ] '<new_port_number>'
 | OS USER '<username>' OS GROUP '<groupname>'
 | FINALIZE REPLICA [ DROP SOURCE DATABASE ]
 | CANCEL REPLICA
 | SYSTEM USER PASSWORD <password>
 | { NO | DEFAULT } RESTART
 | ENCRYPTION CONFIGURATION CONTROLLED BY LOCAL DATABASE
 | [ PERSISTENCE | LOG | BACKUP ] ENCRYPTION [ ON | OFF ]
 | { CREATE | DROP } FALLBACK SNAPSHOT
 | <key_management_spec_list>
```

## Syntax Elements

#### database_name

Specifies the name of the tenant database to which the change is applied.

```sql
<database_name> ::= <identifier>
```

#### alter_service_spec_list

Adds or removes a service, or alters the port of a service.

```sql
<alter_service_spec_list> ::= <alter_service_spec> [<alter_service_spec>…]
<alter_service_spec> ::=
 ADD '<service_type>' [ AT [ LOCATION ] '<hostname>[:<port_number>]' ]
 | REMOVE '<service_type>' AT [ LOCATION ] '<hostname>:<port_number>'
```

##### service_type

Specifies the service type to add.

```sql
<service_type> ::= indexserver | xsengine | scriptserver | dpserver |
diserver | docstore
```

See the SAP HANA Administration Guide for more information about services.

##### hostname

Specifies the host name where the tenant database is located.

##### port_number

Specifies the port number for the host name where the tenant database is located.

#### new_port_number

Specifies a different port number for the host name where the tenant database is located.

#### username

Changes the user name.

```sql
<username> ::= <identifier>
```

#### groupname

Changes the OS user and OS group.

```sql
<groupname> ::= <identifier>
```

The tenant database must be offline to change the user and group. The user and group must already exist. If you specify `OS USER '' OS GROUP ''`, then it is interpreted as `OS USER 'sidadm' OS GROUP 'sapsys'`.

#### FINALIZE REPLICA

Stops replication and finalizes the copy of the tenant database. Use this syntax when the replication status is ACTIVE.

#### DROP SOURCE DATABASE

Drops the original tenant database in the source system.

#### CANCEL REPLICA

Cleans up the system. Use this syntax when you cannot create a new replica because the replication status of the source database is REPLICATING even though the target database has been dropped. Execute this statement from the source database (the one that is being replicated).

#### SYSTEM USER PASSWORD password

Specifies a new system user password for the tenant database.

#### {NO | DEFAULT } RESTART

Specifies the restart mode for the tenant database after a system restart.

DEFAULT restores the previous state of the tenant database before the system restart. For example, if the tenant database was not started before the system restart, it is not started after the system restart. This is the default behavior.

NO specifies to not restart the tenant database after a system restart.

#### ENCRYPTION CONFIGURATION CONTROLLED BY LOCAL DATABASE

Specifies that encryption is controlled by the specified tenant database.

#### [ PERSISTENCE | LOG | BACKUP ] ENCRYPTION [ ON | OFF ]

Turns encryption on or off for the specified tenant database. This command only works if the system database controls the encryption configuration of the tenant.

#### { CREATE | DROP } FALLBACK SNAPSHOT

Creates or removes a fallback snapshot for the tenant database, respectively. A fallback snapshot can be used to restart a tenant database at the point in time that the fallback snapshot was created. There is only one fallback snapshot per tenant database. For more information about fallback snapshots, see the SAP HANA Tenant Databases Guide.

#### key_management_spec_list

Defines the key management operations that you can set.

```sql
<key_management_spec_list> ::=
<add_key_management>
 | <update_key_management>
 | <activate_key_management>
 | <drop_key_management>
```

##### add_key_management

Add a key management configuration for a specific tenant database.

```sql
<add_key_management> ::=
ADD KEY MANAGEMENT CONFIGURATION <config_name> PROPERTIES '<settings>'
```

**config_name** Species a unique name consisting of uppercase letters only, for example, 'AWS_HSM'. The name 'DEFAULT' is forbidden.

###### settings

Creates a JSON document with key-value settings. The list of keys and their supported values depends on the chosen KMS or HSM. The command will fail if the specified settings do not work.

##### update_key_managemet

Alters a key management configuration for a specific tenant database.

```sql
<add_key_management> ::=
ALTER KEY MANAGEMENT CONFIGURATION <config_name> PROPERTIES '<updates>'
```

###### updates

Modifies a JSON document with the new key-value settings. The list of keys and their supported values depends on the chosen HSM or KMS. All settings not described in the update remain unchanged.

**activate_key_management** Activate a key management configuration for a specific tenant database.

```sql
<activate_key_management> ::=
ACTIVATE KEY MANAGEMENT CONFIGURATION <config_name>
```

##### drop_key_management

Remove a key management configuration for a specific tenant database.

```sql
<drop_key_management> ::=
DROP KEY MANAGEMENT CONFIGURATION <config_name>
```

## Description

Lets you make changes to the database. Resetting the system user password is an audited action on both systemdb and on the tenant. Also, the tenant database must be shutdown before resetting the system user password.

Removing a service by using the ALTER DATABASE statement does not cause the remaining services to be re-distributed automatically.

## Permissions

The use of this statement requires the DATABASE ADMIN system privilege.

To use the `<key_management_spec_list>` clause, you must also have the ENCRYPTION ROOT KEY ADMIN system privilege.

## Examples

Add the service `scriptserver` to the tenant database `my_database` at `hostA`, port `30303`.

```sql
ALTER DATABASE my_database ADD 'scriptserver' AT LOCATION 'hostA:30303';
```

Change the port number for service `scriptserver`:

```sql
ALTER DATABASE my_database ALTER 'scriptserver' AT 'hostA:30303' TO '30340';
```

Set the OS user for tenant database `my_database`:

```sql
ALTER DATABASE my_database OS USER 'KPC28' OS GROUP 'admin';
```

Finalize the replica for tenant database `my_database` and drop the source database:

```sql
ALTER DATABASE my_database FINALIZE REPLICA DROP SOURCE DATABASE;
```

Cancel the replica for tenant database `my_database`:

```sql
ALTER DATABASE my_database CANCEL REPLICA;
```

Set the system user password on tenant database `my_database` to `fhu37656`:

```sql
ALTER DATABASE my_database SYSTEM USER PASSWORD fhu37656;
```

Set the restart mode for tenant database `my_database` to not restart after a system restart:

```sql
ALTER DATABASE my_database NO RESTART;
```

Set control of encryption configuration to tenant database `my_database`:

```sql
ALTER DATABASE my_database ENCRYPTION CONFIGURATION CONTROLLED BY LOCAL DATABASE;
```

Turn on log file encryption for tenant database `my_database`:

```sql
ALTER DATABASE my_database LOG ENCRYPTION ON;
```

Drop the fall back snapshot for tenant database `my_database`:

```sql
ALTER DATABASE my_database DROP FALLBACK SNAPSHOT;
```

## Related Information

ALTER SYSTEM START DATABASE Statement (Tenant Database Management) [→](4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-START-DATABASE-Statement-Tenant-Database.md) M_SNAPSHOTS System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SNAPSHOTS-System-View.md) M_DATABASES System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_DATABASES-System-View.md)
