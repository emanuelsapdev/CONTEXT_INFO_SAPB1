# 4.10.1.19.10 ALTER SYSTEM ALTER CONFIGURATION Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 482–485

Sets or removes configuration parameters in an INI file.

## Syntax

```sql
ALTER SYSTEM ALTER CONFIGURATION ( <filename>, <layer>[, <layer_name> ] )
 { SET | UNSET } <parameter_key_value_list>
 [ WITH RECONFIGURE ]
 [ COMMENT <comment_string> ]
```

## Syntax Elements

#### filename

The filename of the configuration file to be modified. If the file does not exist on the required layer, the file is created when a SET command is used.

```sql
<filename> ::= <string_literal>
```

#### layer

Sets the target layer for the configuration change. This parameter can be 'SYSTEM', 'HOST' or 'DATABASE'. The SYSTEM layer is the recommended layer for customer settings. The HOST layer should generally only be used for minor configuration, for example parameters contained in `daemon.ini`. In multitenant systems, system configuration files have an additional layer `DATABASE` to facilitate the configuration of properties for individual databases.

```sql
<layer> ::= <'HOST' | 'SYSTEM' | 'DATABASE'>
```

#### layer_name

If the layer parameter above is set to 'HOST', `<layer_name>` is used to target either a tenant name or a target host name. For example, 'selxeon12' would target the 'selxeon12' host.

```sql
<layer_name> ::= <string_literal>
```

> **Note**
>
> The 'HOST' value must be provided in lowercase only.

#### SET

Updates the value of a key if the key already exists, or inserts a new key if required.

#### UNSET

Removes a key and its associated value.

#### parameter_key_value_list

A list of configuration file entries to be modified or removed.

```sql
<parameter_key_value_list> ::= <parameter_key_value_entry>
   [{, <parameter_key_value_entry>}...]
```

##### parameter_key_value_entry

Specifies the section, key and value of the `.ini` file parameter to be created, modified, or removed.

```sql
<parameter_key_value_entry> ::= (<section_name>,<parameter_name>)
   [ = <parameter_value>]
```

##### section_name

Specifies the section name of the parameter to be modified

```sql
<section_name> ::= <string_literal>
```

##### parameter_name

Specifies the name of the parameter to be modified.

```sql
<parameter_name> ::= <string_literal>
```

##### parameter_value

Specifies the value of the parameter.

```sql
<parameter_value> ::= <string_literal>
```

#### WITH RECONFIGURE

Specifies that the configuration changes are directly applied to the running SAP HANA database instance.

When WITH RECONFIGURE is not specified the configuration changes are written to the required `.ini` file, however the modified values are not applied to the current running system. The changes are only applied during a restart of the SAP HANA database or a subsequent configuration change with WITH RECONFIGURE. In this case there can be inconsistencies between the `.ini` file contents and the actual configuration value that the SAP HANA database is currently using.

#### COMMENT comment_string

Specifies a free-text comment (string literal) that could be used to explain why an `.ini` file parameter is being changed.

## Description

Sets or removes configuration parameters in an INI file. INI file configuration is used for the layered configuration of DEFAULT, SYSTEM, HOST layers. The DEFAULT layer configuration parameters cannot be changed or removed using this command.

By default, an error is returned if a settings is set to an unsupported value. You can control this behavior by using the unsupported_configuration_change parameter in the `global.ini` file.

The following is an example of `.ini` file locations:

- DEFAULT: `/usr/sap/<SYSTEMNAME>/HDB<INSTANCENUMBER>/exe/config/indexserver.ini`
- SYSTEM: `/usr/sap/<SYSTEMNAME>/SYS/global/hdb/custom/config/indexserver.ini`
- HOST: `/usr/sap/<SYSTEMNAME>/HDB<INSTANCENUMBER>/<HOSTNAME>/indexserver.ini`

The priority of the configuration layers is as follows: DEFAULT < SYSTEM < HOST.

Databasespecific configuration files are located in the directory `/hana/shared/$SID/global/hdb/ custom/config/DB_<dbname>`.

The layer that has the highest priority is the HOST layer, followed by the SYSTEM layer and finally the DEFAULT layer. The configuration with the highest priority is applied to the running environment. If the highest priority level configuration is removed, then the configuration with the next highest priority is applied.

For a list of configuration parameters, see the SAP HANA Configuration Parameter Reference.

## Example

You set a parameter new_test_value in the alt_sys_test section of the `global.ini` file.

```sql
ALTER SYSTEM ALTER CONFIGURATION ('global.ini', 'SYSTEM')
   SET ('alt_sys_test', 'new_test_value') = 'test';
```

You set the memory manager's allocation limit setting to 50000 and provide a comment regarding the change:

```sql
ALTER SYSTEM ALTER CONFIGURATION ('indexserver.ini', 'DATABASE', 'C11')
 SET ('memorymanager', 'allocationlimit') = '500000'
 WITH RECONFIGURE
 COMMENT 'Reverting to previous setting';
```

## Related Information

M_INIFILES System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_INIFILES-System-View.md) M_INIFILE_CONTENT_HISTORY System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_INIFILE_CONTENT_HISTORY-System-View.md) M_INIFILE_CONTENTS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_INIFILE_CONTENTS-System-View.md)
