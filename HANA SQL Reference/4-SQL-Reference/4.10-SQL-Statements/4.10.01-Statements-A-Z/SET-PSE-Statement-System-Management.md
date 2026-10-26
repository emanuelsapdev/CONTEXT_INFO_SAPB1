# 4.10.1.146 SET PSE Statement (System Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1097–1099

Sets a purpose for a PSE store.

## Syntax

```sql
SET PSE <pse_name> PURPOSE <purpose> [ FOR <purpose_object_list> ]
```

## Syntax Elements

#### pse_name

Specifies the name of the PSE store.

```sql
<pse_name> ::= <identifier>
```

#### PURPOSE purpose

Specifies the purpose of the PSE.

```sql
<purpose> ::=
 JWT
 | SAML
 | SAP LOGON
 | SSL
 | X509
 | LDAP
 | SOLACE
 | DATABASE REPLICATION
 | REMOTE SOURCE
```

#### purpose_object_list

Specifies the providers, remote sources, and hosts to assign to an existing PSE that has no purpose objects assigned.

```sql
<purpose_object_list> ::=
{ PROVIDER <provider_list> | HOST <host_list> | REMOTE SOURCE
<remote_source_list> }
<provider_list> ::= <provider> [ , <provider>[ ,...] ]
<provider> ::= <simple_identifier>
<host_list> ::= <host> [ ,<host>[ ,...] ]
<remote_source_list> ::= <remote_source> [, <remote_source> [,...] ]
<remote_source> ::= <simple_identifier>
```

PROVIDER can only be specified for a PSE with purpose SAML or JWT. HOST can only be specified for a PSE with purpose SSL. REMOTE SOURCE can only be specified for a PSE with purpose REMOTE SOURCE.

For JWT and SAML, the provider must exist before it can be added. See CREATE JWT PROVIDER Statement and CREATE SAML PROVIDER Statement. For REMOTE SOURCE, the remote source must exist before it can be added. See CREATE REMOTE SOURCE Statement.

Duplicates defined in `<provider_list>` , `<remote_source>`, or `<host_list>` are ignored.

Host names are case insensitive and should exclude the port number (for example, example.sap.corp). The host name format is validated, but its existence in the topology is not. If duplicate host names are present, then the first match from the SNI context list is used. The same host name can be assigned to multiple PSEs.

Multiple providers, remote sources, or hosts can be assigned to a single purpose, but a provider, remote source, or host can only be assigned to one PSE.

When assigning a provider, remote source, or host to a PSE, if the purpose provider or host already exists for another PSE, then the provider, remote source, or host is reassigned to the new PSE. If this results in no remaining purpose providers, remote source, or hosts for the original PSE, then the PSE purpose is removed from the original PSE.

For an existing PSE, to remove all assigned providers, remote source, or hosts from a purpose, but keep the purpose, execute the SET PSE statement without the FOR `<purpose_object_list>` clause. The purpose of the PSE becomes unqualified.

To remove specific providers, remote source, or hosts from a PSE, use ALTER PSE with the `<drop_purpose_object_clause>` clause.

## Permissions

If you are not the owner of the PSE store, then you must have the REFERENCES privilege on the PSE object. For the SSL purpose, you must also have the SSL ADMIN system privilege. For the SAML or JWT purposes, you must also have the USER ADMIN system privilege. For all other authentication purposes, you must also have the TRUST ADMIN privilege. To set the REMOTE SOURCE purpose you must have the system privilege CREATE SOURCE.

## Description

The purpose of a PSE can be qualified or unqualified. A PSE with an unqualified purpose has no provider or host assigned. This kind of PSE is used for authentication when no other PSE with the given purpose matches the provider or host of an incoming authentication request. A PSE with a qualified purpose has one or more providers or hosts assigned. This kind of PSE is preferred over a PSE with an unqualified purpose.

A PSE store with purpose JWT must contain a valid X509 certificate to validate the JWT.

To change the purpose of an existing PSE, you must first execute the UNSET PSE statement to remove the existing purpose from the PSE and then use the SET PSE statement to add a new purpose for the PSE.

## Examples

Set the purpose SAP LOGON for the example_ pse PSE store:

```sql
SET PSE example_pse PURPOSE SAP LOGON;
```

Set the SSL purpose for the PSE1 PSE store using host host1.sap.corp

```sql
SET PSE PSE1 PURPOSE SSL FOR HOST 'host1.sap.corp';
```

Set the REMOTE SOURCE purpose for the HDD_PSE store using HDB_SYS.

```sql
SET PSE HDB_PSE PURPOSE REMOTE SOURCE FOR REMOTE SOURCE HDB_SYS;
```

## Related Information

CREATE JWT PROVIDER Statement (Access Control) [→](CREATE-JWT-PROVIDER-Statement-Access-Control.md) CREATE SAML PROVIDER Statement (Access Control) [→](CREATE-SAML-PROVIDER-Statement-Access-Control.md) ALTER PSE Statement (System Management) [→](ALTER-PSE-Statement-System-Management.md) PSE_PURPOSE_OBJECTS System View [→](../../../6-System-Views-Reference/6.01-System-Views/PSE_PURPOSE_OBJECTS-System-View.md) CREATE REMOTE SOURCE Statement (Access Control) [→](CREATE-REMOTE-SOURCE-Statement-Access-Control.md) SET PSE Statement (System Management) [→](SET-PSE-Statement-System-Management.md) UNSET [SESSION] Statement (Session Management) [→](UNSET-SESSION-Statement-Session-Management.md)
