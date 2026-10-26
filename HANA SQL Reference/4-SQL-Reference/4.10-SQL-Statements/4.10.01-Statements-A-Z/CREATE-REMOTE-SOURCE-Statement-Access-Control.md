# 4.10.1.59 CREATE REMOTE SOURCE Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 755–757

Defines an external data source that can connect to the SAP HANA database.

## Syntax

```sql
CREATE REMOTE SOURCE <remote_source_name> <adapter_clause>
[ <credential_clause> ]
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

Specifies the corresponding adapter, and the type of access method, to be used by the SAP HANA database to access the data. Query the ADAPTERS system view for the list of adapter names you can specify.`

```sql
<adapter_name> ::= <identifier>
```

##### configuration_file

Specifies the configuration file for the specified adapter.

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
<credential_clause> ::= WITH CREDENTIAL TYPE <credential_type> [ USING
<credentials> ]
```

##### credential_type

Supported credential types:

```sql
<credential_type> ::= { 'KERBEROS' | 'PASSWORD' | 'JWT' }
```

- PASSWORD: requires a cleartext user name and password to be used as credential information
- KERBEROS: uses the existing Kerberos configuration
- JWT: uses JSON Web Token (JWT) single sign-on (SSO) for smart data access (SDA)

##### USING credentials

Specifies the user name and password for `<credential_type>` PASSWORD.

```sql
<credentials> ::= 'user=<user_name>;password=<password>'
```

## Permissions

This statement requires the CREATE REMOTE SOURCE privilege.

## Description

For more information on creating remote sources, see Creating a Remote Source in the SAP HANA Administration Guide.

## Example

This example creates a remote source named HOSTA on the hadoop adapter. Details for the remote Hadoop configuration are passed via the `webhdfs.url` and `webhcat.url` key/value pairs. The credentials user dbuser and password dbtest are passed to the remote system.

```sql
CREATE REMOTE SOURCE HOSTA ADAPTER hadoop
    CONFIGURATION 'webhdfs.url=http://hosta:50070/;webhcat.url=http://host:50111'
    WITH CREDENTIAL TYPE 'PASSWORD' USING 'user=dbuser;password=DBtest123';
```

This example creates a remote source named HOSTB on the HANA adapter. Details for the remote ODBC configuration are passed via the `libodbcHDB.so` driver. Kerberos is used for authentication.

```sql
CREATE REMOTE SOURCE HOSTB ADAPTER hanaodbc
    CONFIGURATION 'Driver=libodbcHDB.so;ServerNode=my_hanaserver:30115;'
    WITH CREDENTIAL TYPE 'KERBEROS';
```

This example create a HANA remote source name HOSTC. Failover on the remote source is enabled. The session variable APPLICATIONUSER is set and optimized mode is enabled for linked database.

```sql
CREATE REMOTE SOURCE HOSTC ADAPTER hanaodbc
    CONFIGURATION 'Driver=livodbcHDB.so;ServerNode=my_hanaserver:
30115,my_failover_hanaserver:30215;
    sessionVariable:APPLICATIONUSER=?;linkeddatabase_mode=optimized]’
    WITH CREDENTIAL TYPE 'PASSWORD' USING 'user=dbuser;password=DBtest123';
```

## Related Information

ALTER REMOTE SOURCE Statement (Access Control) [→](ALTER-REMOTE-SOURCE-Statement-Access-Control.md) ADAPTERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/ADAPTERS-System-View.md)
