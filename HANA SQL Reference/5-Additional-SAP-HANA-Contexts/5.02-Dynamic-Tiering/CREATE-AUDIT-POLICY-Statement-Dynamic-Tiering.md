# 5.2.15 CREATE AUDIT POLICY Statement [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1274–1279

Creates a new audit policy for extended tables.

## Syntax

```sql
CREATE AUDIT POLICY <policy_name> AUDITING <audit_status>
   <audit_actions> LEVEL <audit_level> <opt_audit_trail_type>
```

## Syntax Elements

#### policy_name

Specifies the name of the audit policy to be created.

```sql
<policy_name> ::= <identifier>
```

#### audit_status

Defines whether successful, unsuccessful or all executions of the specified audit actions are audited.

```sql
<audit_status> ::=
SUCCESSFUL
| UNSUCCESSFUL
| ALL
```

#### audit_actions

Specifies the audit actions for the audit policy.

```sql
<audit_actions> ::=
 <actions_for_user>
 | <audit_action_list>
 | <target_audit_action_list>
```

##### actions_for_user

Specifies that commands executed by a user or a set of users or all users except the named set of users are audited.

```sql
<actions_for_user> ::= ACTIONS [EXCEPT] FOR <user_name>[{, <user_name>}...]
```

##### user_name

Specifies the username of the user to be audited by the audit policy.

```sql
<user_name> ::= <identifier>
```

##### audit_action_list

Audits specific system actions, optionally limited to a user or a set of users or audited for all users except for the given set of users.

```sql
 <audit_action_list> ::=
<audit_action_name>[{, <audit_action_name>}...]
   [ [EXCEPT] FOR <user_name>[{, <user_name>}...]]
<audit_action_name> ::=
CREATE EXTENDED STORAGE
   | ALTER EXTENDED STORAGE
   | DROP EXTENDED STORAGE
```

For more information on audit actions, see the table of audit actions provided in the **Description** section of this topic.

##### target_audit_action_list

Audits actions on a database object or set of objects. Optionally this auditing can be limited to a user or a set of users or audited for all users except for the given set of users.

```sql
<target_audit_action_list> ::=
 <target_audit_action_entry> [[EXCEPT] FOR <user_name>[{, <user_name>}...]

<target_audit_action_entry> ::=
 <target_audit_action_name>[{, <target_audit_action_name>}...]
   ON <audit_object_name>[{, <audit_object_name>}...]
<target_audit_action_name> ::=
 INSERT
 | UPDATE
 | DELETE
 | SELECT
 | EXECUTE
```

Only objects of type table, view, procedure, and schema can be specified in the `<target_audit_action_entry>`. In case of `<schema_name>`.\*, all objects that are stored in this schema and can be combined with the specified `<target_audit_action_name>` values are audited.

Synonyms and sequences cannot be selected as objects for audit policies. Only specified `<target_audit_action_name>` values can be combined with an object.

##### audit_object_name

```sql
<audit_object_name> ::=
 <table_name>
 | <view_name>
 | <procedure_name>
 | <schema_name>.*
<table_name> ::= [<schema_name>.]<identifier>
<view_name> ::= [<schema_name>.]<identifier>
<procedure_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

Specifies a database object for the target audit action.

#### audit_level

Assigns an audit policy to an audit level.

```sql
<audit_level> ::=
 EMERGENCY
 | ALERT
 | CRITICAL
 | WARNING
 | INFO
```

Possible levels, in decreasing order of importance, are:

- EMERGENCY
- ALERT
- CRITICAL
- WARNING
- INFO

#### opt_audit_trail_type

Specifies the audit trail target type(s) for the audit policy.

```sql
<opt_audit_trail_type> ::= TRAIL TYPE <audit_trail_type_list>
<audit_trail_type_list> ::= <audit_trail_type_name> [,
<audit_trail_type_name> [,…] ]
<audit_trail_type_name> ::=
 TABLE
 | SYSLOG
 | CSV
```

## Permissions

You must have the AUDIT ADMIN privilege.

## Description

The CREATE AUDIT POLICY statement for dynamic tiering creates a new audit policy. This audit policy can then be enabled and results in the auditing of the specified audit actions to occur.

The specified audit policy name must be unique and not match the name of an existing audit policy.

An audit policy defines which audit actions are audited. Audit policies need to be enabled for auditing to occur.

One audit policy can contain one of the following:

- Non-restricted auditing for n (>=1) users
- Auditing for actions not restricted to objects
- Auditing for actions which are restricted to objects.

For the last two alternatives listed, an optional restriction for user(s) is available.

Audit actions (like CREATE/ALTER/DROP/START/STOP DATABASE) can only be specified in the systemDB.

For auditing to occur, audit policies have to be created and enabled. Also the configuration parameter global_auditing_state (see Configuration Parameters) has to be set to true.

One or more audit trail targets can be specified for an audit policy at the time of creation or after creation (see ALTER AUDIT POLICY [Dynamic Tiering] [→](ALTER-AUDIT-POLICY-Statement-Dynamic-Tiering.md)).

The allowed audit trail targets are:

- SYSLOG: uses the system syslog.
- TABLE: stores audit information in database table. The audit log is accessible using AUDIT_LOG system view.
- CSV: stores audit information as comma-separated values in a text file. Should be used only for testing purposes.

### Audit Actions

The table below contains the available audit actions. Each of the audit actions is in a specific group, audit actions in the same group can be combined into one audit policy. At any time, you can retrieve the list of possible audit actions mentioned in this table by executing the following statement: `SELECT * FROM AUDIT_ACTIONS ORDER BY action_group, action_name;`.

| **Audit Action Name** | **Group Number** | **Audit Operation** | **Comment** |
| --- | --- | --- | --- |
| CREATE EXTENDED STORAGE | 20 | creation of the extended store |   |
| ALTER EXTENDED STORAGE | 20 | changes to the extended store |   |
| DROP EXTENDED STORAGE | 20 | deletion of the extended store |   |

## Configuration Parameters

Currently the configuration parameter for auditing is stored in global.ini configuration file, in the auditing configuration section.

```sql
global_auditing_state ( 'true' / 'false' )
```

Activates / deactivates auditing globally, regardless of the enabled state of the audit policies. The default is false, meaning: no auditing occurs.

```sql
default_audit_trail_type ( 'SYSLOGPROTOCOL' / 'CSTABLE' / 'CSVTEXTFILE' )
```

Specifies how to store the auditing results. SYSLOGPROTOCOL is the default.

- SYSLOGPROTOCOL: uses the system syslog.
- CSTABLE: stores audit information in database table. The audit log is accessible using AUDIT_LOG system view.
- CSVTEXTFILE: stores audit information as comma-separated values in a text file. Should be used only for testing purposes.

```sql
default_audit_trail_path
```

Specifies the audit file storage location for the CSVTEXTFILE audit trail type.

```sql
emergency_audit_trail_type
```

Specifies the audit trail target(s) for the events with severity EMERGENCY.

```sql
alert_audit_trail_type
```

Specifies the audit trail target(s) for the events with severity ALERT.

```sql
critical_audit_trail_type
```

Specifies the audit trail target(s) for the events with severity CRITICAL .

Multiple audit trail targets could be specified for parameters emergency_audit_trail_type / alert_audit_trail_type / critical_audit_trail_type by separating the trail type names with comma. To store the auditing information for events with severity EMERGENCY to both Syslog and database table, set the value of emergency_audit_trail_type to 'CSTABLE,SYSLOGPROTOCOL'

As for all configuration parameters, these parameters can be selected in view M_INIFILE_CONTENTS, assuming that the current user has the required privileges. These parameters can only be seen if they have been explicitly set.

## Example

You create a new audit policy named `ext_store_admin_policy` to audit successful attempts to create, alter, or drop extended storage. The audit policy has the medium audit level CRITICAL.

This policy has to be explicitly enabled (see ALTER AUDIT POLICY [Dynamic Tiering] [→](ALTER-AUDIT-POLICY-Statement-Dynamic-Tiering.md)) to cause the auditing of the audit policy.

```sql
CREATE AUDIT POLICY ext_store_admin_policy CREATE EXTENDED STORAGE, ALTER
EXTENDED STORAGE, DROP EXTENDED STORAGE LEVEL CRITICAL
```

You enable auditing of INSERT and UPDATE on an extended table:

```sql
CREATE SCHEMA MY_SCHEMA OWNED BY SYSTEM;
CREATE COLUMN TABLE MY_SCHEMA.MY_EXT_TABLE (A INT PRIMARY KEY, B INT)
USING EXTENDED STORAGE;
CREATE AUDIT POLICY EXT_OBJECT_AUDIT
AUDITING SUCCESSFUL INSERT, UPDATE ON MY_SCHEMA.MY_EXT_TABLE
LEVEL INFO;
ALTER AUDIT POLICY EXT_OBJECT_AUDIT ENABLE;
INSERT into MY_SCHEMA.MY_EXT_TABLE values ( 1, 2 );
INSERT into MY_SCHEMA.MY_EXT_TABLE values ( 3, 4 );
UPDATE MY_SCHEMA.MY_EXT_TABLE SET A = 2 WHERE A = 3;
```

## Related Information

AUDIT_LOG System View [→](../../6-System-Views-Reference/6.01-System-Views/AUDIT_LOG-System-View.md) AUDIT_POLICIES System View [→](../../6-System-Views-Reference/6.01-System-Views/AUDIT_POLICIES-System-View.md) M_INIFILE_CONTENTS System View [→](../../6-System-Views-Reference/6.02-Monitoring-Views/M_INIFILE_CONTENTS-System-View.md)
