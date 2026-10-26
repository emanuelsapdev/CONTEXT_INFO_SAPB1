# 5.2.7 ALTER SYSTEM ALTER CONFIGURATION Statement [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](../README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1236–1239

Sets or removes configuration parameters in an ini file.

## Syntax

```sql
ALTER SYSTEM ALTER CONFIGURATION (<filename>, <layer>[, <layer_name>])
   {SET | UNSET} <parameter_key_value_list> [WITH RECONFIGURE]
```

## Syntax Elements

#### filename

The filename of the configuration file to be modified. If the file does not exist on the required layer, the file is created when a SET command is used.

```sql
<filename> ::= <string_literal>
```

#### layer

Sets the target layer for the configuration change. This parameter can be 'SYSTEM', 'HOST' or 'DATABASE'. The SYSTEM layer is the recommended layer for customer settings. The HOST layer should generally only be used for minor configuration, for example parameters contained in daemon.ini. In multitenant systems, system configuration files have an additional layer `DATABASE` to facilitate the configuration of properties for individual databases.

```sql
<layer> ::= <string_literal>
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

Specifies the section, key and value of the ini file parameter to be created, modified or removed.

```sql
<parameter_key_value_entry> ::= (<section_name>,<parameter_name>)
   [ = <parameter_value>]
```

###### section_name

Specifies the section name of the parameter to be modified

```sql
<section_name> ::= <string_literal>
```

###### parameter_name

Specifies the name of the parameter to be modified.

```sql
<parameter_name> ::= <string_literal>
```

###### parameter_value

Specifies the value of the parameter.

```sql
<parameter_value> ::= <string_literal>
```

#### WITH RECONFIGURE

Specifies that the configuration changes are directly applied to the running SAP HANA database instance.

When WITH RECONFIGURE is not specified the configuration changes are written to the required ini file, however the modified values are not applied to the current running system. The changes are only applied during a restart of the SAP HANA database or a subsequent configuration change with WITH RECONFIGURE. In this case there can be inconsistencies between the ini file contents and the actual configuration value that the SAP HANA database is currently using.

## Permissions

You must have the EXTENDED STORAGE ADMIN and INIFILE ADMIN system privileges.

## Description

Sets or removes configuration parameters in an ini file. Ini file configuration is used for the layered configuration of DEFAULT, SYSTEM, HOST layers.

> **Note**
>
> The DEFAULT layer configuration parameters cannot be changed or removed using this command.

The following is an example of ini file locations:

- DEFAULT: /usr/sap/`<SYSTEMNAME>`/HDB`<INSTANCENUMBER>`/exe/config/indexserver.ini
- SYSTEM: /usr/sap/`<SYSTEMNAME>`/SYS/global/hdb/custom/config/indexserver.ini
- HOST: /usr/sap/`<SYSTEMNAME>`/HDB`<INSTANCENUMBER>`/`<HOSTNAME>`/indexserver.ini
- DATABASE LAYER: /usr/sap/`<SYSTEMNAME>`/HBD/custom/config/DV_`<dbname>`/esserver.ini

The priority of the configuration layers is as follows: DEFAULT < SYSTEM < HOST < DATABASE.

This means that the layer that has the highest priority is the DATABASE layer, followed by the HOST layer, followed by the SYSTEM layer and finally the DEFAULT layer. The configuration with the highest priority is applied to the running environment. If the highest priority level configuration is removed, then the configuration with the next highest priority is applied.

For extended storage, the following are the modifications you can make for configuration parameters:

- You can modify `esserver.ini` on a systemdb or tenantdb connectio.n
- You can modify `global.ini` on a systemdb connection.
- When connected to systemdb, you can modify at the SYSTEM or DATABASE layer for a specific tenant database.
- When connected to a tenant database, you can modify at the SYSTEM layer. Since you are connected to tenant, SYSTEM implies the tenant itself. Specifying DATABASE is unnecessary, and doing so returns an error message.

## Example

You set a parameter new_test_value in the alt_sys_test section of the global.ini file.

```sql
ALTER SYSTEM ALTER CONFIGURATION ('global.ini', 'SYSTEM')
   SET ('alt_sys_test', 'new_test_value') = 'test';
```

You check the setting of the parameter in the SAP HANA studio. In the SAP HANA Systems view, right click on the system where you made the change and select Administration then select the Configuration tab. Expand the global.ini configuration file and then the alt_sys_test section. You unset the new_test_value parameter set in the previous step.

```sql
ALTER SYSTEM ALTER CONFIGURATION ('global.ini', 'SYSTEM')
   UNSET ('alt_sys_test', 'new_test_value');
```

You check the removal of the parameter by clicking refresh on the Configuration page in the SAP HANA studio.

You set the basepath for the data volumes and apply it to the running database.

```sql
ALTER SYSTEM ALTER CONFIGURATION ('esserver.ini', 'SYSTEM')
SET ('persistence' 'basepath_datavolumes_es') = '/path/to/data/volumes' WITH
RECONFIGURE
```

## Related Information

M_INIFILES System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_INIFILES-System-View.md) M_INIFILE_CONTENTS System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_INIFILE_CONTENTS-System-View.md) M_INIFILE_CONTENTS System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_INIFILE_CONTENTS-System-View.md) M_INIFILES System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_INIFILES-System-View.md)

## Contenido de esta sección

- [5.2.7.1 Dynamic Tiering Service Properties (esserver.ini)](5.02.07.01-Dynamic-Tiering-Service-Properties-esserver-ini.md)
- [5.2.7.2 Global System Properties (global.ini)](5.02.07.02-Global-System-Properties-global-ini.md)
