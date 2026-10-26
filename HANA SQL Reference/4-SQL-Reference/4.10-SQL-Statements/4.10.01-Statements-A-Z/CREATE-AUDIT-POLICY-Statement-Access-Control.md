# 4.10.1.43 CREATE AUDIT POLICY Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 684–699

Creates an audit policy.

## Syntax

```sql
CREATE AUDIT POLICY <policy_name> [ FOR <database_name> ] AUDITING
<audit_status> <audit_actions>
   LEVEL <audit_level> [ <opt_audit_trail_type> ]
```

## Syntax Elements

#### policy_name

Specifies the name of the audit policy to be created.

```sql
<policy_name> ::= <identifier>
```

**database_name** Defines the name of the tenant the audit policy applies to. Only one tenant can be specified for each audit policy and this option can only be used when creating audit policies on SYSTEMDB.

#### audit_status

Defines whether successful, unsuccessful, or all executions of the specified audit actions are audited.

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
<actions_for_user> ::= ACTIONS [ EXCEPT ] FOR <user_name> [, <user_name>
[,...] ]
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
   <audit_action_name> [, <audit_action_name> [,...] ]
   [ [ EXCEPT ] FOR <user_name> [ , <user_name> [,...] ]
```

For the complete list of possible values for `<audit_action_name>`, see the table of audit actions provided in the **Description** section of this topic.

##### target_audit_action_list

Audits actions on a database object or a set of objects. Optionally, this auditing can be limited to a user or a set of users or audited for all users except for the given set of users.

```sql
<target_audit_action_list> ::=
 <target_audit_action_entry> [ [ EXCEPT ] FOR <user_name> [, <user_name>
[,...] ]

<target_audit_action_entry> ::=
 <target_audit_action_name> [ , <target_audit_action_name> [,...] ]
   ON <audit_object_name> [ , <audit_object_name> [,...] ]
<target_audit_action_name> ::=
 INSERT
 | UPDATE
 | DELETE
 | SELECT
 | EXECUTE
```

Only tables, views, procedures, and schemas can be specified in the `<target_audit_action_entry>`. In the case of `<schema_name>`.\*, all objects that are stored in this schema and can be combined with the specified `<target_audit_action_name>` values are audited. Synonyms and sequences cannot be selected as objects for audit policies. Only specified `<target_audit_action_name>` values can be combined with an object.

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

The levels are listed above in decreasing order of importance.

#### opt_audit_trail_type

Specifies the audit trail target type(s) for the audit policy.

```sql
<opt_audit_trail_type> ::= TRAIL TYPE <audit_trail_type_list>
<audit_trail_type_list> ::= <audit_trail_type_name> [,
<audit_trail_type_name> [,...] ]
<audit_trail_type_name> ::=
 TABLE [ RETENTION <duration> ]
 | SYSLOG
 | CSV
<duration> ::= <integer>
```

**RETENTION duration** Specifies the length of time the policy is retained, expressed in days. A minimum allowed value can be configured with the configuration parameter [auditing configuration] minimum_retention_period. The default is 7 days.

## Description

The CREATE AUDIT POLICY statement creates a new audit policy, which monitors when specified audit actions occur. Only database users with the AUDIT ADMIN privilege can create an audit policy. An audit policy name must be unique.

New audit policies are disabled by default and must be enabled before the audit actions begin. The configuration parameter global_auditing_state must also be set to true.

An audit policy can contain only one of the following:

- non-restricted auditing for n (>=1) users
- auditing for actions not restricted to objects
- auditing for actions that are restricted to objects

For the last two alternatives listed, an optional restriction for user(s) is available.

Audit actions related to tenant databases (like CREATE/ALTER/DROP/START/STOP DATABASE) can only be specified in the SYSTEMDB of a tenant (database) system.

### Audit Actions

One or more audit trail targets can be specified for an audit policy at the time of creation or after creation. The allowed audit trail targets are:

- SYSLOG: uses the system syslog.
- TABLE: stores audit information in database table. The audit log is accessible using AUDIT_LOG system view.
- CSV: stores audit information as comma-separated values in a text file. Use only for testing purposes.

A subset of audit actions are allowed in policies created on SYSTEMDB for a tenant using the FOR `<database_name>` option. Audit policies created for a tenant on SYSTEMDB cannot be altered or dropped from within that tenant. It must be done on SYSTEMDB.

| **Audit Action Name** | **Group Number** | **Audit Operation** | **SYSTEMDB Supported** |
| --- | --- | --- | --- |
| CANCEL SESSION | 1 - Session Management and System Configuration | Audits the use of ALTER SYS TEM CANCEL SESSION to cancel sessions. | No |
| CONNECT | 1 - Session Management and System Configuration | Audits the creation of a user connection to the database. | Yes |
| DISCONNECT SESSION | 1 - Session Management and System Configuration | Audits the use of ALTER SYS TEM DISCONNECT SESSION to disconnect sessions. | No |
| STOP SERVICE | 1 - Session Management and System Configuration | Audits the stopping of services. | No |
| SYSTEM CONFIGURATIONCHANGE | 1 - Session Management and System Configuration | Audits changes to the system configuration, such as the IN IFILE. | Yes |
| VALIDATE USER | 1 - Session Management and System Configuration | Audits the validation of a user's credentials. | Yes |
| GRANT ANY | 2 - Granting and Revoking of Authorization | Audits the granting of privileges, structured privileges, or roles to users or roles. | No |
| GRANT APPLICATION PRIVILEGE | 2 - Granting and Revoking of Authorization | Audits the granting of application privileges to users or roles. | No |
| GRANT PRIVILEGE | 2 - Granting and Revoking of Authorization | Audits the granting of privileges to users or roles. | No |
| GRANT ROLE | 2 - Granting and Revoking of Authorization | Audits the granting of roles to users or roles. | No |
| GRANT STRUCTURED PRIVILEGE | 2 - Granting and Revoking of Authorization | Audits the granting of structured/analytical privileges to users or roles. | No |
| REVOKE ANY | 2 - Granting and Revoking of Authorization | Audits the revoking of privileges, structured privileges, or roles from users or roles. | No |
| REVOKE APPLICATION PRIVILEGE | 2 - Granting and Revoking of Authorization | Audits the revoking of application privileges from users or roles. | No |
| REVOKE PRIVILEGE | 2 - Granting and Revoking of Authorization | Audits the revoking of privileges from users or roles. | No |
| REVOKE ROLE | 2 - Granting and Revoking of Authorization | Audits the revoking of roles from users or roles. | No |
| REVOKE STRUCTUREDPRIVILEGE | 2 - Granting and Revoking of Authorization | Audits the revoking of structured/analytical privileges from users or roles. | No |
| DELETE | 3 - Data Query and Manipulation | Audits the deletion of rows from tables/views and the truncation of tables. Allows the specification of target objects. | No |
| EXECUTE | 3 - Data Query and Manipulation | Audits the execution of procedure calls. Allows the specification of target objects. | No |
| INSERT | 3 - Data Query and Manipulation | Audits the use of INSERT/ REPLACE/UPSERT statements on tables and views. Allows the specification of target objects. | No |
| SELECT | 3 - Data Query and Manipulation | Audits the use of SELECT statements on tables and views. Allows specification of target objects. | No |
| UPDATE | 3 - Data Query and Manipulation | Audits the use of UPDATE/ REPLACE/UPSERT statements on tables and views. Allows specification of target objects. | No |
| ALTER ROLE | 4 - User and Role Management | Audits the alteration of roles. | No |
| ALTER USER | 4 - User and Role Management | Audits the alteration of users. | No |
| ALTER USERGROUP | 4 - User and Role Management | Audits the alteration of user groups. | No |
| CREATE ROLE | 4 - User and Role Management | Audits the creation of roles. | No |
| CREATE USER | 4 - User and Role Management | Audits the creation of users. | No |
| CREATE USERGROUP | 4 - User and Role Management | Audits the creation of user groups. | No |
| DROP ROLE | 4 - User and Role Management | Audits the dropping of roles. | No |
| DROP USER | 4 - User and Role Management | Audits the dropping of users. | No |
| DROP USERGROUP | 4 - User and Role Management | Audits the dropping of user groups. | No |
| ALTER STRUCTURED PRIVILEGE | 7 - Structured Privilege Management | Audits the altering of the structured/analytical privilege. | No |
| CREATE STRUCTURED PRIVILEGE | 7 - Structured Privilege Management | Audits the creation of the structured/analytical privilege. | No |
| DROP STRUCTURED PRIVILEGE | 7 - Structured Privilege Management | Audits the dropping of the structured/analytical privilege. | No |
| SET SYSTEM LICENSE | 8 - License Installation | Audits the installation of system licenses. | Yes |
| UNSET SYSTEM LICENSE | 9 - License Deletion | Audits the deletion of licenses. | Yes |
| ACTIVATE REPOSITORYCONTENT | 10 - Repository Privilege Management | Audits the activation of repository design time objects. | No |
| EXPORT REPOSITORY CONTENT | 10 - Repository Privilege Management | Audits the export of repository design time objects. | No |
| IMPORT REPOSITORY CONTENT | 10 - Repository Privilege Management | Audits the import of repository design time objects. | No |
| ALTER FULLTEXT INDEX | 11 - Data Definition | Audits the alteration of full text indexes. | No |
| ALTER FUNCTION | 11 - Data Definition | Audits the alteration of functions. | No |
| ALTER GEOCODE INDEX | 11 - Data Definition | Audits the alteration of geocode indexes. | No |
| ALTER INDEX | 11 - Data Definition | Audits the alteration of indexes. | No |
| ALTER PROCEDURE | 11 - Data Definition | Audits the alteration of procedures. | No |
| ALTER SEQUENCE | 11 - Data Definition | Audits the alteration of sequences. | No |
| ALTER STATISTICS | 11 - Data Definition | Audits the alteration of statistics. | No |
| ALTER TABLE | 11 - Data Definition | Audits the alteration of tables. | No |
| ALTER VIEW | 11 - Data Definition | Audits the alteration of views. | No |
| ALTER WORKLOAD CLASS | 11 - Data Definition | Audits the alteration of work load classes. | No |
| ALTER WORKLOAD MAPPING | 11 - Data Definition | Audits the alteration of work load mappings. | No |
| CREATE FULLTEXT INDEX | 11 - Data Definition | Audits the creation of full text indexes. | No |
| CREATE FUNCTION | 11 - Data Definition | Audits the creation of functions. | No |
| CREATE GEOCODE INDEX | 11 - Data Definition | Audits the creation of geocode indexes. | No |
| CREATE GRAPH WORKSPACE | 11 - Data Definition | Audits the creation of graph workspaces. | No |
| CREATE INDEX | 11 - Data Definition | Audits the creation of indexes. | No |
| CREATE PROCEDURE | 11 - Data Definition | Audits the creation of procedures. | No |
| CREATE SEQUENCE | 11 - Data Definition | Audits the creation of sequences. | No |
| CREATE STATISTICS | 11 - Data Definition | Audits the creation of statistics. | No |
| CREATE SYNONYM | 11 - Data Definition | Audits the creation of synonyms. | No |
| CREATE SCHEMA | 11 - Data Definition | Audits the creation of schemas. | No |
| CREATE TABLE | 11 - Data Definition | Audits the creation of tables. | No |
| CREATE TRIGGER | 11 - Data Definition | Audits the creation of triggers. | No |
| CREATE VIEW | 11 - Data Definition | Audits the creation of views. | No |
| CREATE WORKLOAD CLASS | 11 - Data Definition | Audits the creation of work load classes. | No |
| CREATE WORKLOAD MAPPING | 11 - Data Definition | Audits the creation of work load mappings. | No |
| DROP FULLTEXT INDEX | 11 - Data Definition | Audits the dropping of full text indexes. | No |
| DROP FUNCTION | 11 - Data Definition | Audits the dropping of functions. | No |
| DROP GEOCODE INDEX | 11 - Data Definition | Audits the dropping of geocode indexes. | No |
| DROP GRAPH WORKSPACE | 11 - Data Definition | Audits the dropping of graph workspaces. | No |
| DROP INDEX | 11 - Data Definition | Audits the dropping of indexes. | No |
| DROP PROCEDURE | 11 - Data Definition | Audits the dropping of procedures. | No |
| DROP SCHEMA | 11 - Data Definition | Audits the dropping of schemas. | No |
| DROP SEQUENCE | 11 - Data Definition | Audits the dropping of sequences. | No |
| DROP STATISTICS | 11 - Data Definition | Audits the dropping of statistics. | No |
| DROP SYNONYM | 11 - Data Definition | Audits the dropping of synonyms. | No |
| DROP TABLE | 11 - Data Definition | Audits the dropping of tables. | No |
| DROP TRIGGER | 11 - Data Definition | Audits the dropping of triggers. | No |
| DROP VIEW | 11 - Data Definition | Audits the dropping of views. | No |
| DROP WORKLOAD CLASS | 11 - Data Definition | Audits the dropping of work load classes. | No |
| DROP WORKLOAD MAPPING | 11 - Data Definition | Audits the dropping of work load mappings. | No |
| REFRESH STATISTICS | 11 - Data Definition | Audits the refreshing of statistics. | No |
| RENAME COLUMN | 11 - Data Definition | Audits the renaming of columns | No |
| RENAME INDEX | 11 - Data Definition | Audits the renaming of indexes | No |
| RENAME TABLE | 11 - Data Definition | Audits the renaming of tables | No |
| ACTIONS | 12 - All Actions | Audits all user-triggered database actions. Used for spe cific users. | No |
| BACKUP CATALOG DELETE | 13 - Backup and Recovery | Audits the deletion of entries in the backup catalog. | No |
| BACKUP DATA | 13 - Backup and Recovery | Audits the backing up of data. | No |
| RECOVER DATA | 13 - Backup and Recovery | Audits the recovery of data. | No |
| ACTIVATE KEY MANAGEMENT CONFIGURATION | 14 - Volume Encryption | Audits the activation of key management configuration. | No |
| ADD KEY MANAGEMENTCONFIGURATION | 14 - Volume Encryption | Audits the addition of key management configuration. | No |
| ALTER APPLICATION ENCRYPTION | 14 - Volume Encryption | Audits the alteration of application encryption keys. | Yes |
| ALTER APPLICATION ENCRYPTION ROOT KEY | 14 - Volume Encryption | Audits the alteration of application encryption root keys. | Yes |
| ALTER BACKUP ENCRYPTION | 14 - Volume Encryption | Audits the alteration of backup encryption status. | Yes |
| ALTER BACKUP ENCRYPTION ROOT KEY | 14 - Volume Encryption | Audits the alteration of backup encryption root keys. | Yes |
| ALTER KEY MANAGEMENTCONFIGURATION | 14 - Volume Encryption | Audits the alteration of key management configuration. | No |
| ALTER LOG ENCRYPTION | 14 - Volume Encryption | Audits the alteration of log encryption status. | Yes |
| ALTER LOG ENCRYPTIONROOT KEY | 14 - Volume Encryption | Audits the alteration of log encryption root keys. | Yes |
| ALTER PERSISTENCE ENCRYPTION | 14 - Volume Encryption | Audits the alteration of data base persistence encryption status and page encryption keys. | Yes |
| ALTER PERSISTENCE ENCRYPTION ROOT KEY | 14 - Volume Encryption | Altering database persistence encryption root keys. | Yes |
| ALTER ROOT KEYS BACKUPPASSWORD | 14 - Volume Encryption | Audits the alteration of the backup password used to protect backup root keys. | Yes |
| DROP KEY MANAGEMENTCONFIGURATION | 14 - Volume Encryption | Audits the dropping of key management configuration. | No |
| ENCRYPTION CONFIG CONTROL | 14 - Volume Encryption | Audits the alteration of the database (system or local tenant database) controlling the encryption configuration. | Yes |
| TENANT BACKUP ENCRYPTION | 14 - Volume Encryption | Audits the switching on or off of the backup encryption for the tenant. | Yes |
| TENANT LOG ENCRYPTION | 14 - Volume Encryption | Audits the switching on or off of the log encryption for the tenant. | Yes |
| TENANT PERSISTENCE ENCRYPTION | 14 - Volume Encryption | Audits the switching on or off of the data volume encryption for the tenant. | No |
| TENANT ROOT KEYSBACKUP PASSWORD | 14 - Volume Encryption | Audits the setting the root key backup password. | No |
| 1CREATE DATABASE | 16 - Operations on Multitenant Database Containers | Creating a database. Available only for the SYSTEMDB in a multitenant database system. | No |
| 1ALTER DATABASE | 16 - Operations on Multitenant Database Containers | Altering a database. Available only for the SYSTEMDB in a multitenant database system. | No |
| 1DROP DATABASE | 16 - Operations on Multitenant Database Containers | Dropping a database. Available only for the SYSTEMDB in a multitenant database system. | No |
| 1RENAME DATABASE | 16 - Operations on Multitenant Database Containers | Renaming a database. Available only for the SYSTEMDB in a multitenant database system. | No |
| 1START DATABASE | 16 - Operations on Multitenant Database Containers | Starting a database. Available only for the SYSTEMDB in a multitenant database system. | No |
| 1STOP DATABASE | 16 - Operations on Multitenant Database Containers | Stopping a database. Available only for the SYSTEMDB in a multitenant database system. | No |
| ALTER ADAPTER | 17 - Data Provisioning | Audits the alteration of adapters. | No |
| ALTER AGENT | 17 - Data Provisioning | Audits the alteration of agents. | No |
| ALTER REMOTE SOURCE | 17 - Data Provisioning | Audits the alteration of remote sources. | No |
| ALTER REMOTE SUBSCRIPTION | 17 - Data Provisioning | Audits the alteration of remote subscriptions. | No |
| CREATE ADAPTER | 17 - Data Provisioning | Audits the creation of adapters. | No |
| CREATE AGENT | 17 - Data Provisioning | Audits the creation of agents. | No |
| CREATE AGENT GROUP | 17 - Data Provisioning | Audits the creation of agent groups. | No |
| CREATE REMOTE SOURCE | 17 - Data Provisioning | Audits the creation of remote sources. | No |
| CREATE REMOTE SUBSCRIPTION | 17 - Data Provisioning | Audits the creation of remote subscriptions. | No |
| DROP ADAPTER | 17 - Data Provisioning | Audits the dropping of adapters. | No |
| DROP AGENT | 17 - Data Provisioning | Audits the dropping of agents. | No |
| DROP AGENT GROUP | 17 - Data Provisioning | Audits the dropping of agent groups. | No |
| DROP REMOTE SOURCE | 17 - Data Provisioning | Audits the dropping of remote sources. | No |
| DROP REMOTE SUBSCRIPTION | 17 - Data Provisioning | Audits the dropping of remote subscriptions. | No |
| PROCESS REMOTE SUBSCRIPTION EXCEPTION | 17 - Data Provisioning | Audits the processing of remote subscription exceptions. | No |
| ALTER EXTENDED STORAGE | 18 - SAP HANA Dynamic Tiering | Audits the altering of extended store. | No |
| CREATE EXTENDED STORAGE | 18 - SAP HANA Dynamic Tiering | Audits the creation of extended store. | No |
| DROP EXTENDED STORAGE | 18 - SAP HANA Dynamic Tiering | Audits the dropping of extended store. | No |
| ALTER PSE | 19 - Certificates and PSE Store | Audits the alteration of PSEs. | Yes |
| CREATE CERTIFICATE | 19 - Certificates and PSE Store | Audits the creation of certificates. | Yes |
| CREATE PSE | 19 - Certificates and PSE Store | Audits the creation of PSEs. | Yes |
| DROP CERTIFICATE | 19 - Certificates and PSE Store | Audits the dropping of certificates. | Yes |
| DROP PSE | 19 - Certificates and PSE Store | Audits the dropping of PSEs. | Yes |
| ALTER JWT PROVIDER | 20 - Authentication Provider Management | Audits the alteration of JWT providers. | Yes |
| ALTER LDAP PROVIDER | 20 - Authentication Provider Management | Audits the alteration of LDAP providers. | Yes |
| ALTER SAML PROVIDER | 20 - Authentication Provider Management | Audits the alteration of SAML providers. | Yes |
| CREATE JWT PROVIDER | 20 - Authentication Provider Management | Audits the creation of JWT providers. | Yes |
| CREATE LDAP PROVIDER | 20 - Authentication Provider Management | Audits the creation of LDAP providers. | Yes |
| CREATE SAML PROVIDER | 20 - Authentication Provider Management | Audits the creation of SAML providers. | Yes |
| DROP JWT PROVIDER | 20 - Authentication Provider Management | Audits the dropping of JWT providers. | Yes |
| DROP LDAP PROVIDER | 20 - Authentication Provider Management | Audits the dropping of LDAP providers. | Yes |
| DROP SAML PROVIDER | 20 - Authentication Provider Management | Audits the dropping of SAML providers. | Yes |
| VALIDATE LDAP PROVIDER | 20 - Authentication Provider Management | Audits the refreshing of LDAP providers. | Yes |
| ALTER CLIENTSIDE ENCRYPTION COLUMN KEY | 21 - Client-side Encryption | Audits the alteration of a column encryption key (CEK). | No |
| ALTER CLIENTSIDE ENCRYPTION KEYPAIR | 21 - Client-side Encryption | Audits the alteration of a client-side encryption key pair. | No |
| CREATE CLIENTSIDE ENCRYPTION COLUMN KEY | 21 - Client-side Encryption | Audits the creation of a CEK. | No |
| CREATE CLIENTSIDE ENCRYPTION KEYPAIR | 21 - Client-side Encryption | Audits the creation of a client-side encryption key pair. | No |
| DROP CLIENTSIDE ENCRYPTION COLUMN KEY | 21 - Client-side Encryption | Audits the dropping of a CEK. | No |
| DROP CLIENTSIDE ENCRYPTION KEYPAIR | 21 - Client-side Encryption | Audits the dropping of a client-side encryption key pair. | No |
| PERSONAL DATA ACCESS | 22 - Application Auditing | Audits audit log access to personal data. | No |
| PERSONAL DATA MODIFICATION | 22 - Application Auditing | Audits audit log modification of personal data. | No |
| CONFIGURATION CHANGE | 22 - Application Auditing | Audits audit log configuration change events. | No |
| SECURITY EVENT | 22 - Application Auditing | Audits audit log security events. | No |
| DEBUGGER ATTACH PROC1ESS | 23 - Procedure Debugging | Audits audit log debugger attachment process events. | No |
| 1DEBUGGER EXECUTION | 23 - Procedure Debugging | Audits audit log debugger execution events. | No |

1

This action can only be added to policies created on SYSTEMDB and does not support the FOR

`<database_name>` option.

## Permissions

To create an audit policy on SYSTEMDB or on a tenant, you must have the AUDIT ADMIN privilege.

To use the FOR `<database_name>` option, you need the DATABASE AUDIT ADMIN privilege granted on SYSTEMDB, not on the tenant.

## Example

Create a new audit policy named priv_audit that audits successful granting and revoking of privileges and roles. The audit policy has the medium audit level CRITICAL.

This policy has to be explicitly enabled to cause the auditing of the audit policy.

```sql
CREATE AUDIT POLICY priv_audit AUDITING SUCCESSFUL GRANT PRIVILEGE, REVOKE
PRIVILEGE, GRANT ROLE, REVOKE ROLE LEVEL CRITICAL;
```

Create a new audit policy named object_audit that audits the inserts into the existing table MY_SCHEMA.MY_TABLE. This policy must be explicitly enabled to cause the auditing of the audit policy. This policy is restricted to user FRED and uses the audit level INFO.

```sql
CREATE USER FRED PASSWORD qw3XtD;
 CREATE SCHEMA MY_SCHEMA OWNED BY system;
 CREATE ROW TABLE MY_SCHEMA.MY_TABLE (first_col int);
 GRANT INSERT ON MY_SCHEMA.MY_TABLE to FRED;
 CREATE AUDIT POLICY OBJECT_AUDIT AUDITING SUCCESSFUL INSERT ON
MY_SCHEMA.MY_TABLE FOR FRED LEVEL INFO;
```

Create a new audit policy named update_object_audit that audits the updates of the existing table MY_SCHEMA.MY_TABLE. This policy must be enabled explicitly to make the auditing of the audit policy occur. The auditing should be done for all users except the existing user TECH_ADMIN. This policy uses the audit level CRITICAL.

```sql
CREATE USER TECH_ADMIN PASSWORD 9gP3us;
 CREATE SCHEMA MY_SCHEMA OWNED BY system;
 CREATE ROW TABLE MY_SCHEMA.MY_TABLE (first_col int);
 GRANT UPDATE ON MY_SCHEMA.MY_TABLE to TECH_ADMIN;
 CREATE AUDIT POLICY UPDATE_OBJECT_AUDIT AUDITING SUCCESSFUL UPDATE ON
MY_SCHEMA.MY_TABLE EXCEPT FOR TECH_ADMIN LEVEL CRITICAL;
```

Create a new audit policy named SYSTEMDB_TEST that audits successful changes to an existing PSE. This policy is set on the SYSTEMDB and applies the tenant HA2.

```sql
CREATE AUDIT POLICY SYSTEMDB_TEST FOR HA2 AUDITING SUCCESSFUL ALTER PSE LEVEL
CRITICAL;
```

## Related Information

AUDIT_POLICIES System View [→](../../../6-System-Views-Reference/6.01-System-Views/AUDIT_POLICIES-System-View.md) ALTER AUDIT POLICY Statement (Access Control) [→](ALTER-AUDIT-POLICY-Statement-Access-Control.md) AUDIT_ACTIONS System View [→](../../../6-System-Views-Reference/6.01-System-Views/AUDIT_ACTIONS-System-View.md)
