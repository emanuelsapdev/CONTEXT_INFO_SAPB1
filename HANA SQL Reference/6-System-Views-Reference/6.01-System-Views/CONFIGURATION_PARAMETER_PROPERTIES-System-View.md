# 6.1.39 CONFIGURATION_PARAMETER_PROPERTIES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1443–1444

Displays metadata and properties of the public configuration parameters for SAP HANA.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SECTION | VARCHAR(128) | Displays the section of the parameter to configure. |
| KEY | VARCHAR(128) | Displays the parameter key. |
| HAS_KEY_INDEX | VARCHAR(9) | Displays whether or not the parameter is indexed: NO, OPTIONAL, or MANDA TORY. |
| DESCRIPTION | NVARCHAR(5000) | Displays a description of the parameter. |
| DATA_TYPE_NAME | VARCHAR(32) | Displays the data type of the parameter. |
| VALUE_LIST_SEPARATOR | VARCHAR(1) | Displays the element separator character for value lists. Returns NULL for simple values. |
| DEFAULT_VALUE | NVARCHAR(5000) | Displays the default value of the parameter. |
| RESTART_REQUIRED | VARCHAR(8) | Displays whether or not a restart is required. The values are: TRUE, FALSE, or CUSTOM. CUSTOM indicates a custom function or callback to decide whether a restart is required or not depending on the new value to be set. |
| INIFILE_NAMES | VARCHAR(32) | Displays the .ini files that can contain the parameter value, for example:`service.ini,` `<service>.ini, global.ini` |
| UNIT | VARCHAR(16) | Displays the unit that the value is measured in, for example, megabytes, kilobytes, seconds, and so on. |
| VALUE_RESTRICTIONS | NVARCHAR(256) | Displays the restrictions for the supported values. |
| CUSTOM_RESTRICTIONS | NVARCHAR(1024) | Displays the description of the custom restriction, if one is defined. |
| LAYER_RESTRICTIONS | VARCHAR(8) | Displays the layer name if a parameter can only be set on specific layers: SYS TEM, HOST, or READONLY. |
| IS_READ_ONLY | VARCHAR(5) | Displays if the parameter is set to read only. |
| IS_SYSTEM_MANAGED | VARCHAR(5) | Displays if a parameter is managed internally by the system. |
| IS_TEMPLATE | VARCHAR(5) | Displays whether the configuration parameter templates or regular parameters are used: TRUE/FALSE. |
