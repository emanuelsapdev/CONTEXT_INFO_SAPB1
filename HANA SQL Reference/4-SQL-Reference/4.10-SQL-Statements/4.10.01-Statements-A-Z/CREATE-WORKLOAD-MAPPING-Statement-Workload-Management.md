# 4.10.1.78 CREATE WORKLOAD MAPPING Statement (Workload Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 882–884

Defines workload mappings.

## Syntax

```sql
CREATE WORKLOAD MAPPING <mapping_name>
WORKLOAD CLASS <workloadclass_name> [ <property_list> [ <wildcard_option> ] ]
```

## Syntax Elements

#### mapping_name

Specifies the name for the new workload mapping.

```sql
<mapping_name> ::= <identifier>
```

#### workloadclass_name

Specifies the workload class name.

```sql
<workloadclass_name> ::= <identifier>
```

#### property_list

Defines the workload mapping properties.

```sql
<property_list> ::=
 { [ SET <key_value_pair_list> ] | [ UNSET <key_value_pair_list> ] }
<key_value_pair_list> ::= <key_value_pair> [, <key_value_pair> [,…] ]
<key_value_pair> ::= '<key>'='<value>'
```

```sql
<key> ::=
APPLICATION USER NAME
 | CLIENT
 | APPLICATION COMPONENT NAME
 | APPLICATION COMPONENT TYPE
 | APPLICATION NAME
 | {USER NAME | USERGROUP NAME}
 | SCHEMA NAME
 | OBJECT NAME
 | XS APPLICATION USER NAME
<value> ::= <string_literal>
```

USERGROUP NAME and USER NAME cannot be configured together. For established connections, changes to USERGROUP NAME are only applied when a connected database client reconnects. If there are two matched workload classes by USER NAME and USERGROUP NAME respectively, then USER NAME takes precedence over USERGROUP NAME.

SCHEMA NAME and OBJECT NAME must be configured together. SCHEMA NAME is the schema of the object. OBJECT NAME can be a procedure name, application function library (AFL) area or package name.

If an AFL area or package name is specified, then the workload class is applied to all AFLLANG procedures that call AFs in that AFL area.

If there are multiple workload classes matched by SCHEMA NAME and OBJECT NAME, then the following order of precedence is used applied: AREA --> PACKAGE --> PROCEDURE.

XS APPLICATION USER NAME takes precedence over APPLICATION USER NAME.

#### wildcard_option

Specifies the wildcard character to use for value matching.

```sql
<wildcard_option> ::= WITH WILDCARD [ <wildcard-character> ]
<wildcard-character> ::= <ASCII_character>
```

Wildcard characters can only be ASCII characters and cannot be used with USER NAME or USERGROUP NAME, SCHEMA NAME, or OBJECT NAME.

Only prefix wildcards are supported, for example WILDCARD %.

If no wildcard character is specified, then the default wildcard character is %. Use one wildcard character per property.

## Permissions

You need the WORKLOAD_ADMIN system privilege.

## Description

This statement defines workload mappings.

Workload mapping settings are stored in the WORKLOAD_MAPPINGS system view.

## Examples

The following statement creates an entry for the MyWorkloadMapping1 workload mapping for the ABCADM database user and the BW application.

```sql
CREATE WORKLOAD MAPPING "MyWorkloadMapping1" WORKLOAD CLASS "MyWorkloadClass"
SET 'USER NAME' = 'ABCADM', 'APPLICATION NAME' = 'BW';
```

The following statement uses the wildcard character % by default for value matching any application name that begins with BW.

```sql
CREATE WORKLOAD MAPPING "MyWorkloadMapping1" WORKLOAD CLASS "MyWorkloadClass"
SET 'APPLICATION NAME' = 'BW%' WITH WILDCARD;
```

The following two statements both result in an error since the wildcard must be placed at the end of the property value.

```sql
CREATE WORKLOAD MAPPING "MyWorkloadMapping1" WORKLOAD CLASS "MyWorkloadClass"
SET 'APPLICATION NAME' = 'BW%123' WITH WILDCARD;
```

```sql
CREATE WORKLOAD MAPPING "MyWorkloadMapping1" WORKLOAD CLASS "MyWorkloadClass"
SET 'APPLICATION NAME' = 'BW%*123' WITH WILDCARD '*';
```

The following statement creates an entry for the MyWorkloadMapping1 workload mapping for the USERGROUP_TEST user group.

```sql
CREATE WORKLOAD MAPPING "MyWorkloadMapping1" WORKLOAD CLASS "MyWorkloadClass"
SET 'USERGROUP NAME' = 'USERGROUP_TEST';
```

The following statement creates an entry for the "MyWorkloadMapping1" workload mapping for the object SYS.CHECK_ES.

```sql
CREATE WORKLOAD MAPPING "MyWorkloadMapping1" WORKLOAD CLASS "DATAMART" 'SCHEMA
NAME' = 'SYS', 'OBJECT NAME' = 'CHECK_ES';
```

The following statement creates an entry for the MyWorkloadMapping1 workload mapping for the XS application user name TESTER.

```sql
CREATE WORKLOAD MAPPING "MyWorkloadMapping1" WORKLOAD CLASS "DATAMART" SET 'XS
APPLICATION USER NAME' = 'TESTER';
```

The following statement uses the wildcard character % by default for any creates XS application user name that begins with ADMIN.

```sql
CREATE WORKLOAD MAPPING "MyWorkloadMapping1" WORKLOAD CLASS "DATAMART" SET 'XS
APPLICATION USER NAME' = 'ADMIN%' WITH WILDCARD;
```

## Related Information

WORKLOAD_MAPPINGS System View [→](../../../6-System-Views-Reference/6.01-System-Views/WORKLOAD_MAPPINGS-System-View.md) ALTER WORKLOAD MAPPING Statement (Workload Management) [→](ALTER-WORKLOAD-MAPPING-Statement-Workload-Management.md)
