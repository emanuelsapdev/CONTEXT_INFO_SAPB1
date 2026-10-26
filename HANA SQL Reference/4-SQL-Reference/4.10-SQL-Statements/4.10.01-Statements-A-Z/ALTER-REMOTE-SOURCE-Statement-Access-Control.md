# 4.10.1.13 ALTER REMOTE SOURCE Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 449–452

Modifies the configuration of an external data source that is connected to an SAP HANA database.

## Syntax

```sql
ALTER REMOTE SOURCE <remote_source_name> [ <adapter_clause> ]
[ <credential_clause> ]
 | ALTER REMOTE SOURCE <remote_source_name> { <refresh_clause> | <drop_clause> }
 | ALTER REMOTE SOURCE <remote_source_name> [ <properties_clause> ]
```

## Syntax Elements

#### remote_source_name

Specifies the identifier of the remote source.

```sql
<remote_source_name> ::= <identifier>
```

#### adapter_clause

Specifies the adapter configuration.

```sql
<adapter_clause> ::=
 [ ADAPTER <adapter_name> [ CONFIGURATION FILE <configuration_file> ]
CONFIGURATION <connection_info_string> ]
```

##### adapter_name

Specifies the adapter to be used to access the remote data. Query the ADAPTERS system view for the list of available adapter names.

```sql
<adapter_name> ::= <identifier>
```

**configuration_file** Specifies the configuration file for the specified adapter.

##### connection_info_string

Specifies the connection parameters for a given adapter.

For an on-premise remote source:

```sql
<connection_info_string> ::=
   { 'DSN=<DSN_entry_name>'
     | ' { webhdfs.url=http://<host_name>:50070/;webhcat.url=http://
<host_name>:50111
         | Driver=<ODBC_library>; ServerNode=<machine_name>:
3<instance#>15 }
       [,<failover_server_name>:3<failover_instance_number>15 ]
       [ ;sessionVariable:<session_variable_name>=? ]
       [ ;linkeddatabase_mode=optimized ] } '
}
```

For an SAP HANA service instance remote source:

```sql
<connection_info_string> ::=
   { 'DSN=<DSN_entry_name>'
     | ' { webhdfs.url=http://<host_name>:50070/;webhcat.url=http://
<host_name>:50111
         | Driver=<ODBC_library>; ServerNode=<tenant_endpoint> }
       [,<failover_tenant_endpoint> ]
       [ ;sslTrustStore="<digi_certificate_string>";encrypt=TRUE; ]
       [ ;sessionVariable:<session_variable_name>=? ]
       [ ;linkeddatabase_mode=optimized ] } '
   }
```

The failover, session variable, and linked database parameters are only supported for SAP HANA remote sources.

#### credential_clause

Specifies the credential configuration.

```sql
<credential_clause> ::= WITH CREDENTIAL TYPE <credential_type> | DROP
CREDENTIAL TYPE [ 'KERBEROS' | 'PASSWORD' ]
```

##### credential_type

Specifies a credential type and the credential.

```sql
<credential_type> ::= TYPE [ 'KERBEROS' | 'PASSWORD' [ USING
<credentials> ] ]
```

**drop_clause** Delete all linked objects associated with a linked database using the remote source.

```sql
<drop_clause> ::= DROP LINKED OBJECTS [ CASCADE | RESTRICT ]
```

The CASCADE option drops all the linked tables and dependent objects associated with linked tables. The RESTRICT option drops linked tables are dropped only if there are no dependencies on any of the linked tables. If this option is used and there are dependent objects on a linked table, then an error is raised, and all linked tables are retained. If no drop option is specified, then all internally generated linked tables with no dependencies are dropped. Linked tables with dependencies are retained.

#### refresh_option

Refreshes metadata for a single linked table or all linked objects using the remote source.

```sql
<refresh_option> ::= REFRESH LINKED { OBJECTS | TABLE <table_name> }
<table_name> ::= <database_name>.<schema_name>.<identifier>
```

`<database_name>` is the name of the remote source. `<identifier>` is the name of the table on the remote source.

#### properties_clause

Changes the value of one or more properties of a single remote source.

```sql
<properties_clause> ::= { SET PROPERTY <prop_definition_list> | UNSET
PROPERTY { ALL | <prop_list> } }
<prop_definition_list> ::= <prop_definition> [, <prop_definition> [ ,... ] ]
<prop_definition> ::= <prop_name> = <prop_value> [ <prop_name> = <prop_value>
[,... ] ]
<prop_list> ::= <prop_name> [ , <prop_name> [ ,... ] ]
```

SET replaces the default property value with a new value. UNSET returns the property value to its default value. For a list of properties that can be set for a remote source, see Listing Remote Source Properties in the SAP HANA Administration Guide.

## Description

For more information on creating remote sources, see the SAP HANA Administration Guide .

## Permissions

This statement requires the ALTER object privilege on the remote source.

## Example

This example alters the remote source MY_REMOTE1 to use the HANA adapter, DSN entry MYHANA1, and set a new technical user credential for the source.

```sql
ALTER REMOTE SOURCE MY_REMOTE1 ADAPTER HANAODBC CONFIGURATION 'DSN=MYHANA1'
   WITH CREDENTIAL TYPE 'PASSWORD' USING 'user="user1";password="Password1"';
```

This example drops the technical user credential for the MY_REMOTE1 remote source.

```sql
ALTER REMOTE SOURCE MY_REMOTE1 DROP CREDENTIAL TYPE 'PASSWORD';
```

This example clears all internally generated objects associated with remote source MY_REMOTE1 and drops any dependent objects that reference the linked object.

```sql
ALTER REMOTE SOURCE MY_REMOTE1 DROP LINKED OBJECTS CASCADE;
```

This example refreshes the metadata of all linked objects associated with remote source MY_REMOT1E.

```sql
ALTER REMOTE SOURCE MY_REMOTE1 REFRESH LINKED OBJECTS;
```

This example refreshes the metadata for remote table MYSCHEMA.MYTABLE on remote source MY_REMOTE1.

```sql
ALTER REMOTE SOURCE MY_REMOTE REFRESH LINKED TABLE MY_REMOTE1.MYSCHEMA.MYTABLE;
```

This example enables failover, sets the session variable APPLICATIONUSER, and enables optimized mode for linked database on the SAP HANA remote source MY_REMOTE1.

```sql
ALTER REMOTE SOURCE MY_REMOTE1 ADAPTER HANAODBC
     CONFIGURATION
'Driver=libodbcHDB.so;ServerNode=my_machine1:30115,failover_machine1:30215
     sessionVariable:APPLICATIONUSER=?;linkeddatabase_mode=optimized]’;
```

This example sets two properties on the remote source RS1

```sql
ALTER REMOTE SOURCE RS1 SET PROPERTY 'CAP_LIMIT' = 'true',
'PROP_USE_UNIX_MANAGER'= 'true';
```

This example unsets all properties on remote source RS1

```sql
ALTER REMOTE SOURCE RS1 UNSET PROPERTY ALL;
```
