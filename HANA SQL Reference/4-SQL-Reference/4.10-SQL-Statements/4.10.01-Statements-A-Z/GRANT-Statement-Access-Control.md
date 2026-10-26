# 4.10.1.119 GRANT Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 952–970

Grants various types of privileges to users and roles.

## Syntax

```sql
GRANT <system_privilege>[{, <system_privilege>}...] TO <grantee> [ WITH ADMIN
OPTION ]
 | GRANT <source_privilege>[{, <source_privilege>}...] ON REMOTE SOURCE
<source_name> TO <grantee> [ WITH GRANT OPTION ]
 | GRANT <schema_privilege>[{, <schema_privilege>}...] ON SCHEMA <schema_name>
TO <grantee> [ WITH GRANT OPTION ]
 | GRANT <object_privilege>[{, <object_privilege>}...] ON <object_name> TO
<grantee> [ WITH GRANT OPTION ]
 | GRANT <column_key_privilege> ON CLIENTSIDE ENCRYPTION COLUMN KEY
<column_encryption_key_name> TO <grantee> [ WITH GRANT OPTION ]
 | GRANT <role_name>[{, <role_name>}...] TO <grantee> [ WITH ADMIN OPTION ]
 | GRANT STRUCTURED PRIVILEGE <privilege_name> TO <grantee>
```

## Syntax Elements

#### grantee

Specifies the user or role that the privilege is being granted to. A role is a named collection of privileges and can be granted to either a user or another role.

```sql
<grantee> :: = <user_name> | <role_name>
```

```sql
<user_name> ::= <unicode_name>
```

```sql
<role_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

If a privilege or role is granted to a role, then all users granted that role have the specified privilege or role.

If you want to allow several database users to perform the same actions, then create a role, grant the required privileges to this role, and finally grant the role to the different database users.

When granting roles to roles, a tree of roles can be built. When granting a role (R) to a role or user (G), user G has all the privileges directly granted to role R and all privileges granted to roles that have been granted to role R.

`<user_name>` specifies the grantee's user name.

`<role_name>` specifies the grantee's role name with optional schema name.

`<schema_name>` specifies the schema containing the database object to be acted upon.

A reference to a schema-local role (that is, a role for which a schema_name was specified at creation time), must always be preceded by its `<schema_name>` wherever it is referenced (for example, `GRANT <schema_name>.<role_name> TO...)`.

#### system_privilege

Grants the specified system privilege.

```sql
<system_privilege> ::=
```

ADAPTER ADMIN

| IMPORT

| AGENT ADMIN

| INIFILE ADMIN

| ALTER CLIENTSIDE ENCRYPTION KEYPAIR

| LDAP ADMIN

| ATTACH DEBUGGER

| LICENSE ADMIN

| AUDIT ADMIN

| LOG ADMIN

| AUDIT OPERATOR

| MONITOR ADMIN

| AUDIT READ

| OPTIMIZER ADMIN

| BACKUP ADMIN

| RESOURCE ADMIN

| BACKUP OPERATOR

| ROLE ADMIN

| CATALOG READ

| SAVEPOINT ADMIN

| CERTIFICATE ADMIN

| SCENARIO ADMIN

| CLIENT PARAMETER ADMIN

| SERVICE ADMIN

| CREATE CLIENTSIDE ENCRYPTION KEYPAIR

| SESSION ADMIN

| CREATE R SCRIPT

| SSL ADMIN

| CREATE REMOTE SOURCE

| STRUCTUREDPRIVILEGE ADMIN

| CREATE SCENARIO

| SYSTEM REPLICATION ADMIN

| CREATE SCHEMA

| TABLE ADMIN

| CREATE STRUCTURED PRIVILEGE

| TRACE ADMIN

| CREDENTIAL ADMIN

| TRUST ADMIN

| DATA ADMIN

| USER ADMIN

| DATABASE ADMIN | VERSION ADMIN

| DATABASE START | WORKLOAD ADMIN

| DATABASE STOP | WORKLOAD ANALYZE ADMIN

| DROP CLIENTSIDE ENCRYPTION KEYPAIR | WORKLOAD CAPTURE ADMIN

| ENCRYPTION ROOT KEY ADMIN | WORKLOAD REPLAY ADMIN

| EXPORT `<identifier>`.`<identifier>`

| \| EXTENDED STORAGE ADMIN |   |
| --- | --- |

System privileges restrict administrative tasks. The following table describes the supported system privileges in an SAP HANA database.

| **System Privilege** | **Description** |
| --- | --- |
| ADAPTER ADMIN | Controls the execution of the following adapter-related statements: CREATE ADAPTER, DROP ADAPTER, and AL TER ADAPTER. It also allows access to the ADAPTERS and ADAPTER_LOCATIONS system views. |
| AGENT ADMIN | Controls the execution of the following agent-related statements: CREATE AGENT, DROP AGENT, and ALTER AGENT. It also allows access to the AGENTS and ADAPTER_LOCATIONS system views. |
| ALTER CLIENTSIDE ENCRYPTION KEYPAIR | Authorizes a user to add a new version of a client-side encryption key pair (CKP), or to drop all older versions of the CKP. |
| ATTACH DEBUGGER | Authorizes debugging across different user sessions. For example, userA can grant ATTACH DEBUGGER to userB to allow userB to debug a procedure in userA’s session (userB still needs DEBUG privilege on the procedure, how ever). |
| AUDIT ADMIN | Controls the execution of the following auditing-related statements: CREATE AUDIT POLICY, DROP AUDIT POL ICY, and ALTER AUDIT POLICY, as well as changes to the auditing configuration. It also allows access to the AUDIT_LOG, XSA_AUDIT_LOG, and ALL_AUDIT_LOG system views. |
| AUDIT OPERATOR | Authorizes the execution of the following statement: AL TER SYSTEM CLEAR AUDIT LOG. It also allows access to the AUDIT_LOG system view. |
| AUDIT READ | Authorizes read-only access to the rows of the AUDIT_LOG, XSA_AUDIT_LOG, and ALL_AUDIT_LOG system views. |
| BACKUP ADMIN | Authorizes BACKUP and RECOVERY statements for defining and initiating backup and recovery procedures. It also authorizes changing system configuration options with respect to backup and recovery. |
| BACKUP OPERATOR | Authorizes the BACKUP statement to initiate a backup. |
| CATALOG READ | Authorizes unfiltered access to the data in the system views that a user has already been granted the SELECT privilege on. Normally, the content of these views is filtered based on the privileges of the user. CATALOG READ does not allow a user to view system views on which they have not been granted the SELECT privilege. |
| CERTIFICATE ADMIN | Authorizes the changing of certificates and certificate collections that are stored in the database. |
| CLIENT PARAMETER ADMIN | Authorizes a user to override the value of the CLIENT parameter for a database connection or to overwrite the value of the $$client$$ parameter in an SQL query. |
| CREATE CLIENTSIDE ENCRYPTION KEYPAIR | Authorizes a user to create client-side encryption key pairs. |
| CREATE R SCRIPT | Authorizes the creation of a procedure by using the language R. |
| CREATE REMOTE SOURCE | Authorizes the creation of remote data sources by using the CREATE REMOTE SOURCE statement. It also allows you to set the purpose of a certificate collection to RE MOTE SOURCE. |
| CREATE SCENARIO | Controls the creation of calculation scenarios and cubes (calculation database). |
| CREATE SCHEMA | Authorizes the creation of database schemas using the CREATE SCHEMA statement. |
| CREATE STRUCTURED PRIVILEGE | Authorizes the creation of structured (analytic privileges).<br>Only the owner of the privilege can further grant or revoke that privilege to other users or roles. |
| CREDENTIAL ADMIN | Authorizes the use of the statements CREATE CREDEN TIAL, ALTER CREDENTIAL, and DROP CREDENTIAL. |
| DATA ADMIN | Authorizes reading all data in the system views. It also enables execution of Data Definition Language (DDL) statements in the SAP HANA database.<br>A user with this privilege cannot select or change data in stored tables for which they do not have access privileges, but they can drop tables or modify table definitions. |
| DATABASE ADMIN | Authorizes all statements related to tenant databases, such as CREATE, DROP, ALTER, RENAME, BACKUP, and RECOVERY. |
| DATABASE START | Authorizes a user to start any database in the system and to select from the M_DATABASES view. |
| DATABASE STOP | Authorizes a user to stop any database in the system and to select from the M_DATABASES view. |
| DROP CLIENTSIDE ENCRYPTION KEYPAIR | Authorizes a user to drop other users' client-side encryption key pairs. |
| ENCRYPTION ROOT KEY ADMIN | Authorizes all statements related to management of root keys:<br>Allows access to the system views pertaining to encryption (for example, ENCRYPTION_ROOT_KEYS, M_ENCRYPTION_OVERVIEW, M_PERSISTENCE_ENCRYPTION_STATUS, M_PERSISTENCE_ENCRYPTION_KEYS, and so on). |
| EXPORT | Authorizes EXPORT to a file on the SAP HANA server. The user must also have the SELECT privilege on the source tables to be exported. |
| EXTENDED STORAGE ADMIN | Authorizes the management of SAP HANA dynamic tiering and the creation of extended storage. |
| IMPORT | Authorizes the import activity in the database using the IMPORT statements. Additional privileges may also be required to be able to execute an IMPORT. See the IMPORT statement for more information. |
| INIFILE ADMIN | Authorizes making changes to system settings. |
| LDAP ADMIN | Authorizes the use of the CREATE \| ALTER \| DROP \| VALI DATE LDAP PROVIDER statements. |
| LICENSE ADMIN | Authorizes the use of the SET SYSTEM LICENSE statement to install a new license. |
| LOG ADMIN | Authorizes the use of the ALTER SYSTEM LOGGING [ON \| OFF] statements to enable or disable the log flush mechanism. |
| MONITOR ADMIN | Authorizes the use of the ALTER SYSTEM statements for events. |
| OPTIMIZER ADMIN | Authorizes the use of the ALTER SYSTEM statements concerning SQL PLAN CACHE and ALTER SYSTEM UPDATE STATISTICS statements, which influence the behavior of the query optimizer. |
| RESOURCE ADMIN | Authorizes statements concerning system resources (for example, the ALTER SYSTEM RECLAIM DATAVOLUME and ALTER SYSTEM RESET MONITORING VIEW statements). It also authorizes use of the Kernel Profiler statements, and many of the statements available in the Management Console. |
| ROLE ADMIN | Authorizes the creation and deletion of roles by using the CREATE ROLE and DROP ROLE statements. It also authorizes the granting and revoking of roles by using the GRANT and REVOKE statements.<br>Activated repository roles, meaning roles whose creator is the predefined user _SYS_REPO, can neither be granted to other roles or users nor dropped directly. Not even users with the ROLE ADMIN privilege can do so. Check the documentation concerning activated objects. |
| SAVEPOINT ADMIN | Authorizes the execution of a savepoint using the ALTER SYSTEM SAVEPOINT statement. |
| SCENARIO ADMIN | Authorizes all calculation scenario-related activities (including creation). |
| SERVICE ADMIN | Authorizes the ALTER SYSTEM [START\|CANCEL\|RECON FIGURE] statements for administering system services of the database. |
| SESSION ADMIN | Authorizes the ALTER SYSTEM commands concerning sessions to stop or disconnect a user session or to change session variables. |
| SSL ADMIN | Authorizes the use of the SET...PURPOSE SSL statement. It also allows access to the PSES system view. |
| STRUCTUREDPRIVILEGE ADMIN | Authorizes the creation, reactivation, and dropping of structured (analytic) privileges. |
| SYSTEM REPLICATION ADMIN | Authorizes the use of ALTER SYSTEM statements related to system replication. |
| TABLE ADMIN | Authorizes LOAD, UNLOAD and MERGE of tables and table placement. |
| TRACE ADMIN | Authorizes the use of the ALTER SYSTEM statements related to database tracing (including the Kernel Profiler feature) and the changing of trace system settings. |
| TRUST ADMIN | Authorizes the use of statements to update the trust store. |
| USER ADMIN | Authorizes the creation and modification of users by using the CREATE \| ALTER \| DROP USER statements. |
| VERSION ADMIN | Authorizes the use of the ALTER SYSTEM RECLAIM VER SION SPACE statement of the multi-version concurrency control (MVCC) feature. |
| WORKLOAD ADMIN | Authorizes execution of the workload class and mapping statements (for example, CREATE \| ALTER \| DROP WORK LOAD CLASS, and CREATE \| ALTER \| DROP WORKLOAD MAPPING). |
| WORKLOAD ANALYZE ADMIN | Used by the Analyze Workload, Capture Workload, and Replay Workload applications when performing workload analysis. |
| WORKLOAD CAPTURE ADMIN | Authorizes access to the monitoring view M_WORKLOAD_CAPTURES to see the current status of capturing and captured workloads, as well of execution of actions with the WORKLOAD_CAPTURE procedure. |
| WORKLOAD REPLAY ADMIN | Authorizes access to the monitoring views M_WORKLOAD_REPLAY_PREPROCESSES and M_WORKLOAD_REPLAYS to see current status of preprocessing, prepro cessed, replaying, and replayed workloads, as well as the execution of actions with the WORKLOAD_REPLAY procedure. |
| `<identifier>`.`<identifier>` | Components of the SAP HANA database can create new system privileges. These privileges use the component-name as the first identifier of the system privilege and the component-privilege-name as the second identifier. |

#### source_privilege

Restricts the access and modification of a source entry.

```sql
<source_privilege> ::=
 CREATE VIRTUAL TABLE
 | DROP
 | LINKED DATABASE
 | REMOTE EXECUTE
```

##### CREATE VIRTUAL TABLE

Authorizes the creation of proxy tables pointing to remote tables from the source entry.

Proxy tables are created in a schema and point to remote entries found in a source.

##### DROP

Authorizes the DROP REMOTE SOURCE statement for the related source entry.

##### LINKED DATABASE

Authorizes execution of linked database queries.

##### REMOTE EXECUTE

Authorizes the use of the REMOTE_EXECUTE_QUERY function on the specified remote sources.

#### schema_privilege

Allows access to and modifications on a schema and the objects stored in the schema.

```sql
<schema_privilege> ::=
 | ALL PRIVILEGES
 | ALTER
 | CLIENTSIDE ENCRYPTION COLUMN KEY ADMIN
 | CREATE ANY
 | CREATE TEMPORARY TABLE
 | CREATE VIRTUAL PACKAGE
 | DEBUG
 | DEBUG MODIFY
 | DELETE
 | DROP
 | EXECUTE
 | INDEX
 | INSERT
 | SELECT
 | SELECT CDS METADATA
 | SELECT METADATA
 | TRIGGER
 | UNMASKED
 | UPDATE
```

The following schema privileges are defined:

##### ALL PRIVILEGES

Grants all existing schema privilege to `<grantee>` with the exception of DEBUG, DEBUG MODIFY, and SQLSCRIPT LOGGING.

Additional privileges added later to the schema must be granted separately, or by executing another GRANT ALL PRIVILEGES statement.

##### ALTER

Allows the modification of all kinds of objects in a schema.

##### CLIENTSIDE ENCRYPTION COLUMN KEY ADMIN

Allows a user to administer column encryption keys (CEKs), including creating, altering and dropping them. Key administrators must have the CLIENTSIDE ENCRYPTION COLUMN KEY ADMIN privilege.

Read access to CEKs is determined by whether a client has a CEK-copy encrypted by a public key of client key pair that is available to them in their local hdbkeystore.

##### CREATE ANY

Allows the creation of all kinds of objects, such as tables, views, sequences, synonyms, triggers, SQLScript functions, graph workspaces, or database procedures, in a schema.

##### CREATE TEMPORARY TABLE

Allows you to create a temporary local table, which can be used as input for procedures, even if the user does not have the CREATE ANY privilege for the corresponding schema.

##### CREATE VIRTUAL PACKAGE

Allows creation of virtual packages for objects, such as functions and procedures, that can be run on remote sources.

##### DELETE, DROP, EXECUTE, INDEX, INSERT, SELECT, UPDATE

The specified privilege is granted on every object stored in the specified schema currently and going forward. For detailed descriptions of the privileges, including which privileges are applicable to different objects, see the table describing object privileges.

##### DEBUG

Allows the use of debug features.

##### DEBUG MODIFY

For internal use only.

##### SELECT CDS METADATA

Allows the selection of CDS metadata from the catalog.

##### SELECT METADATA

Allows the selection of metadata for one schema from the catalog. This privilege includes access to the object definition in the case of a view, procedure, function, or trigger that may be located in different schemas.

##### TRIGGER

Allows you to create, alter, drop, enable, and disable triggers.

##### UNMASKED

Authorizes access to masked data in tables and userdefined views. This privilege is required to view the original data in views and tables that are defined with the WITH MASK clause.

#### object_privilege

Restricts access to, and modification of, database objects.

```sql
<object_privilege> ::=
 ALL PRIVILEGES
 | ALTER
 | CREATE ANY
 | CREATE OBJECT STRUCTURED PRIVILEGE
 | CREATE VIRTUAL FUNCTION
 | CREATE VIRTUAL PACKAGE
 | CREATE VIRTUAL PROCEDURE
 | CREATE VIRTUAL TABLE
| DEBUG
| DEBUG MODIFY
| DELETE
| DROP
| EXECUTE
| INDEX
| INSERT
| REFERENCES
| SELECT
| SELECT CDS METADATA
| SELECT METADATA
| TRIGGER
| REMOTE TABLE ADMIN
| UNMASKED
| UPDATE
| USERGROUP OPERATOR
| <identifier>.<identifier>
```

For synonyms, the same restrictions apply to the synonym as they do for the object that the synonym represents.

The following table describes the supported object privileges in an SAP HANA database.

| **Object Privilege** | **Command Types** | **Applies to** | **Privilege Description** |
| --- | --- | --- | --- |
| ALL PRIVILEGES | DDL & DML | • Schemas<br>• Tables<br>• Views | This privilege is a collection of all Data Definition Language (DDL) and Data Manipulation Language (DML) privileges that the grantor currently possesses and is allowed to grant further. The privilege it grants is specific to the particular object being acted upon.<br>This privilege collection is dynamically evaluated for the given grantor and object. |
| ALTER | DDL | • Schemas<br>• Tables<br>• Views<br>• Functions/procedures | Authorizes the ALTER statement for the object. |
| CREATE ANY | DDL | • Schemas<br>• Tables<br>• Views<br>• Sequences<br>• Functions/procedures<br>• Remote sources<br>• Graph workspaces<br>• Triggers | Authorizes all CREATE statements for the object. |
| CREATE OBJECT STRUCTURED PRIVILEGE | DDL | • Schemas<br>• Views | Authorizes creation of structured privilege commands on the object even if the user does not need to have the CREATE STRUC TURED PRIVILEGE. |
| CREATE VIRTUAL FUNCTION | DDL | • Remote sources | Authorizes creation of virtual functions (the REFER ENCES privilege is also required). |
| CREATE VIRTUAL PROCEDURE | DDL | • Remote sources | Authorizes creation of virtual procedure to create and run procedures on a remote source. |
| CREATE VIRTUAL PACKAGE | DDL | • Schemas | Authorizes creation of virtual packages that can be run on remote sources. |
| CREATE VIRTUAL TABLE | DDL | • Remote sources | Authorizes the creation of proxy tables pointing to remote tables from the source entry. |
| CREATE TEMPORARY TABLE | DDL | • Schemas | Authorizes the creation of a temporary local table, which can be used as input for procedures, even if the user does not have the CREATE ANY privilege for the schema. |
| DEBUG | DML | • Schemas<br>• Calculation Views<br>• Functions/procedures | Authorizes debug functionality for the procedure or calculation view or for the procedures and calculation views of a schema. |
| DEBUG MODIFY | DDL | • Functions/procedures | For internal use only. |
| DELETE | DML | • Schemas<br>• Tables<br>• Views<br>• Functions/procedures | Authorizes the DELETE and TRUNCATE statements for the object.<br>While DELETE applies to views, it only applies to updatable views (that is, views that do not use a join, do not contain a UNION, and do not use aggregation). |
| DROP | DDL | • Schemas<br>• Tables<br>• Views<br>• Sequences<br>• Functions/procedures<br>• Remote sources<br>• Graph workspaces | Authorizes the DROP statements for the object. |
| EXECUTE | DML | • Schemas<br>• Functions/procedures | Authorizes the execution of a SQLScript function or a database procedure by using the CALLS or CALL statement respectively. It also allows a user to execute a virtual function. |
| INDEX | DDL | • Schemas<br>• Tables | Authorizes the creation, modification, or dropping of indexes for the object. |
| INSERT | DML | • Schemas<br>• Tables<br>• Views | Authorizes the INSERT statement for the object.<br>The INSERT and UPDATE privilege are both required on the object to allow the REPLACE and UPSERT statements to be used.<br>While INSERT applies to views, it only applies to updatable views (views that do not use a join, do not contain a UNION, and do not use aggregation). |
| REFERENCES | DDL | • Schemas<br>• Tables | Authorizes the usage of all tables in this schema or this table in a foreign key definition, or the usage of a personal security environment (PSE). It also allows a user to reference a virtual function package. |
| REMOTE TABLE ADMIN | DDL | • Remote sources | Authorizes the creation of tables on a remote source object. |
| SELECT | DML | • Schemas<br>• Tables<br>• Views<br>• Sequences<br>• Graph workspaces | Authorizes the SELECT statement for the object or the usage of a sequence. When selection from system-versioned tables, users must have SELECT on both the table and its associated history table. |
| SELECT CDS METADATA | DML | • Schemas<br>• Tables | Authorizes access to CDS metadata from the catalog. |
| SELECT METADATA | DML | • Schemas<br>• Tables | Authorizes access to the complete metadata of all objects in a schema (including procedure and view definitions), including objects that may be located in other schemas. |
| TRIGGER | DDL | • Schemas<br>• Tables | Authorizes the CREATE/ ALTER/DROP/ENABLE and DISABLE TRIGGER statements for the specified table or the tables in the specified schema. |
| UNMASKED | DML | • Schemas<br>• Views<br>• Tables | Authorizes access to masked data in user-defined views and tables. This privilege is required to view the original data in views and tables that are defined by using the WITH MASK clause. |
| UPDATE | DML | • Schemas<br>• Tables<br>• Views | While UPDATE applies to views, it only applies to updatable views (views that do not use a join, do not contain a UNION, and do not use aggregation). |
| USERGROUP OPERATOR | DML | • User groups | Authorizes a user to change the settings for a user group, and to add and re move users to/from a user group.<br>Users with the USERGROUP OPERATOR privilege can also create and drop users, but only within the user group they have the USERGROUP OPERATOR privilege on (CREATE USER `<user_name>` SET USERGROUP `<usergroup_name>`).<br>A user can have the USERGROUP OPERATOR privilege on more than one user group, and a user group can have more than one user with the USERGROUP OPERATOR privilege on it.<br>When granting USERGROUP OPERATOR to a user group, you must include the keyword USERGROUP before the name of the user group (for example: `GRANT` `USERGROUP OPERATOR ON USERGROUP <usergroup> TO` `<grantee>`). This is slightly differenct syntax than granting USERGROUP OPERATOR to a user. |
| `<identifier>`.`<identifi` `er>` | DDL |   | Components of the SAP HANA database can create new object privileges. These privileges use the component-name as first identifier of the system privilege and the component-privilege-name as the second identifier. |

#### column_key_privilege

Specifies a column key privilege. Currently only USAGE is supported.

```sql
<column_key_privilege> ::= USAGE
```

#### object_name

```sql
<object_name> ::=
 <table_name>
 | <view_name>
 | <sequence_name>
 | <procedure_name>
 | <synonym_name>
```

```sql
<table_name> ::= [<schema_name>.]<identifier>
```

```sql
<view_name> ::= [<schema_name>.]<identifier>
```

```sql
<sequence_name> ::= [<schema_name>.]<identifier>
```

```sql
<procedure_name> ::= [<schema_name>.]<identifier>
```

```sql
<synonym_name> ::= [<schema_name>.]<identifier>
```

#### column_encryption_key_name

Specifies a column encryption key name for use with client-side encryption.

```sql
<column_encryption_key_name> ::= [<schema_name>.]<identifier>
```

#### privilege_name

Grants the specified privilege.

```sql
<privilege_name> ::= <identifier>
```

#### WITH ADMIN OPTION and WITH GRANT OPTION

Specifies that the granted privileges can be granted further by the specified user or by users with the specified role.

#### GRANT s PRIVILEGE privilege_name

Grants a previously defined analytic privilege based on a generic structured privilege to a user or role.

This analytic privilege restricts the access for read operations to certain data in Analytic, Attribute, and Calculation Views by filtering the attribute values.

## Description

The GRANT statement grants privileges and structured privileges to users and roles. It also grants roles to users and other roles.

The default schema for a user always has the same schema name as the user.

## Permissions

To use the GRANT statement to grant privileges to other users and roles, a user must have the privilege and also the permissions required to grant that privilege.

**SYSTEM, non-RESTRICTED users, and RESTRICTED users**: A SYSTEM user has all system privileges and the role PUBLIC. However, a SYSTEM user cannot select or change data in another user's tables unless this privilege has been explicitly granted. A non-RESTRICTED user has the PUBLIC role, has the privileges required to create objects in their own default schema, and can grant privileges on their objects to other users and roles. A RESTRICTED user does not have the PUBLIC role and cannot create objects in their own schemas. RESTRICTED users have only the privileges that have been explicitly granted to them.

Users can not grant privileges to themselves.

For objects that are dependent on other objects, like views being dependent on tables, there may be times when the owner of the dependent object does not have a complete set of privileges. This situation can occur if the user does not have privileges on the underlying objects on which their object depends.

## Examples

Create a schema called `my_schema`.

```sql
CREATE SCHEMA my_schema;
```

Create a table named `work_done` in the `my_schema` schema.

```sql
CREATE ROW TABLE my_schoolwork_done (t TIMESTAMP, user NVARCHAR (256), work_done
VARCHAR (256));
```

Create a new user named worker with password `His_Password_1`.

```sql
CREATE USER worker PASSWORD His_Password_1;
```

Create a role called `role_for_work_on_my_schema`.

```sql
CREATE ROLE role_for_work_on_my_schema;
```

Grant the SELECT privilege on any object in `my_schema` to the `role_for_work_on_my_schema`.

```sql
GRANT SELECT ON SCHEMA my_schema TO role_for_work_on_my_schema;
```

Grant the INSERT privilege for the `my_schoolwork_done` table to the `role_for_work_on_my_schema`.

```sql
GRANT INSERT ON my_schoolwork_done TO role_for_work_on_my_schema;
```

Grant the `role_for_work_on_my_schema` role to the worker user.

```sql
GRANT role_for_work_on_my_schema TO worker WITH ADMIN OPTION;
```

Grant the DELETE privilege for the `my_schoolwork_done table` to the `worker` user.

```sql
GRANT DELETE ON my_schoolwork_done TO worker;
```

Grant the `worker` user the privilege to create any kind of object in the schema named `my_schema`.

```sql
GRANT CREATE ANY ON SCHEMA my_schema TO worker;
```

The result of the above statements is that the worker user has the privilege to SELECT all tables and views in schema my_schema, to INSERT into and DELETE from table `my_schoolwork_done`, and to create objects in schema `my_schema`. Additionally the worker user can grant DELETE on the table `myschema.work_done` to other users and roles.

Grant the INIFILE ADMIN and TRACE ADMIN privileges to the user `worker`. You grant these privileges along with the permission for the worker user to grant them further.

```sql
GRANT INIFILE ADMIN, TRACE ADMIN TO worker WITH ADMIN OPTION;
```

Grant the LINKED DATABASE privilege to user `myuser1` to execute linked database queries by using the remote source `myremotesys`.

```sql
GRANT LINKED DATABASE ON REMOTE SOURCE myremotesys TO myuser1;
```

Grant the USAGE privilege on a column encryption key `my_cek` to user `User1`, with the ability for `User1` to grant the privilege to others:

```sql
GRANT USAGE ON CLIENTSIDE ENCRYPTION COLUMN KEY my_cek TO User1 WITH GRANT
OPTION;
```

Grant the CLIENTSIDE ENCRYPTION COLUMN KEY ADMIN privilege to user `KeyAdministrator` to allow to manage CEKs on schema `MySchema`:

```sql
GRANT CLIENTSIDE ENCRYPTION COLUMN KEY ADMIN ON SCHEMA MySchema TO
KeyAdministrator;
```

## Related Information

REVOKE Statement (Access Control) [→](REVOKE-Statement-Access-Control.md) USERGROUPS System View [→](../../../6-System-Views-Reference/6.01-System-Views/USERGROUPS-System-View.md)

CLIENTSIDE_ENCRYPTION_COLUMN_KEYS System View [→](../../../6-System-Views-Reference/6.01-System-Views/CLIENTSIDE_ENCRYPTION_COLUMN_KEYS-System-View.md) USERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/USERS-System-View.md) USERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/USERS-System-View.md) ROLES System View [→](../../../6-System-Views-Reference/6.01-System-Views/ROLES-System-View.md) GRANTED_ROLES System View [→](../../../6-System-Views-Reference/6.01-System-Views/GRANTED_ROLES-System-View.md) GRANTED_PRIVILEGES System View [→](../../../6-System-Views-Reference/6.01-System-Views/GRANTED_PRIVILEGES-System-View.md) IMPORT Statement (Data Import Export) [→](IMPORT-Statement-Data-Import-Export.md)
