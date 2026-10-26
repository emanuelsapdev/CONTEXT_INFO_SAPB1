# 4.10.1.12 ALTER PSE Statement (System Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 445–449

Modifies a PSE store.

## Syntax

```sql
ALTER PSE <pse_name> { <add_certificate_clause>
   | <drop_certificate_clause>
   | <set_own_certificate_clause>
   | <unset_own_certificate_clause>
   | <add_purpose_object_clause>
   | <drop_purpose_object_clause> }
```

## Syntax Elements

#### pse_name

Specifies the name of the PSE store to be altered.

```sql
<pse_name> ::= <identifier>
```

#### add_certificate_clause

Adds the certificate(s) to the PSE store.

```sql
<add_certificate_clause> ::= ADD CERTIFICATE ( <certificate_id> [ ,
<certificate_id> ]...)
<certificate_id> ::= <unsigned_integer>
```

A PSE that is assigned a purpose can only be changed by a user who owns that specific PSE, or a user with the ALTER privilege on this PSE who also has the privilege to assign this PSE this purpose.

#### drop_certificate_clause

Drops the certificate(s) from the PSE store.

```sql
<drop_certificate_clause> ::= DROP CERTIFICATE ( <certificate_id> [ ,
<certificate_id> ]...)
<certificate_id> ::= <unsigned_integer>
```

A PSE that is assigned a purpose can only be changed by a user who owns that specific PSE or a user with the ALTER privilege on this PSE and in addition has the privilege to assign this PSE this purpose.

#### set_own_certificate_clause

Sets an own certificate and private key.

```sql
<set_own_certificate_clause> ::= SET OWN CERTIFICATE <certificate_content>
<certificate_content> ::= <string_literal>
```

The string `<certificate_content>` may contain one or several certificates in the PEM format and the private key of the own certificate. One of the certificates is the own certificate and the other certificate(s) are intermediate chain certificates completing the trust chain from the own certificate to the root certificate which the peer trusts. The own certificate and the order of the certificates forming a chain can be identified by the issuer or subject relationship. In case the PSE Store already has an own certificate assigned, it is replaced. **unset_own_certificate_clause** Removes an own certificate and private key.

```sql
<unset_own_certificate_clause> ::= UNSET OWN CERTIFICATE
```

#### add_purpose_object_clause

Specifies the providers, hosts, or remote sources to add to an existing PSE that already has at least one purpose object assigned.

```sql
<add_purpose_object_clause> ::=
ADD { PROVIDER <provider_list> | HOST <host_list> | REMOTE SOURCE
<remote_source_list> }
<provider_list> ::= <provider>[ , <provider> [ ,...] ]
<provider> ::= <simple_identifier>
<host_list> ::= <host> [ ,<host> [ ,...] ]
<remote_source_list> ::= <remote_source> [, <remote_source> [,...] ]
<remote_source> ::= <simple_identifier>
```

PROVIDER can only be specified for a PSE with purpose SAML, JWT, or X509. HOST can only be specified for a PSE with purpose SSL. REMOTE SOURCE can only be specified for a PSE with purpose REMOTE SOURCE.

For JWT, SAML, and X509, the provider must exist before it can be added. See CREATE JWT PROVIDER Statement, CREATE SAML PROVIDER Statement, and CREATE X509 PROVIDER Statement. For REMOTE SOURCE, the remote source must exist before it can be added. See CREATE REMOTE SOURCE Statement.

Duplicates defined in `<provider_list>` , `<remote_source>`, or `<host_list>` are ignored.

Host names are case insensitive and should exclude the port number (for example, example.sap.corp). The host name format is validated but not its existence in the topology. If duplicate host names are present, the first match from the SNI context list is used. The same host name can be assigned to multiple PSE.

Multiple providers, remote sources, or hosts can be assigned to a single purpose, but a provider, remote source, or host can only be assigned to one PSE.

When adding a provider, remote source, or host to a PSE, if the purpose provider, remote source, or host already exists for another PSE, the provider, remote source, or host is reassigned to the new PSE. If this results in no remaining purpose providers, remote source, or hosts for the original PSE, the PSE purpose is removed from the original PSE.

Use the SET PSE statement with the `<purpose_object_list>` clause, not the ALTER PSE statement with the `<add_purpose_object_clause>` clause to add or reassign a purpose provider, remote source, or host to an existing PSE that does not have at least one provider, remote source, or host assigned.

#### drop_purpose_object_clause

Specifies the providers, remote source, or hosts to drop from an existing PSE.

```sql
<drop_purpose_object_clause> ::= DROP { PROVIDER <provider_list> | HOST
<host_list> | REMOTE SOURCE <remote_source_list> }
<provider_list> ::= <provider> [ , <provider> [ ,...] ]
<provider> ::= <simple_identifier>
<host_list> ::= <host> [ ,<host> [ ,...] ]
<remote_source_list> ::= <remote_source> [, <remote_source> [,...] ]
<remote_source> ::= <simple_identifier>
```

PROVIDER can only be specified for a PSE with purpose SAML or JWT. HOST can only be specified for a PSE with purpose SSL. REMOTE SOURCE can only be specified for a PSE with purpose REMOTE SOURCE.

To drop the last purpose provider, remote source, or host from a PSE, use the SET PSE statement without the `<purpose_object_list>` clause.

## Description

Modifies a PSE store.

## Permissions

To use the purpose object clauses on an SSL purpose, you must have the SSL ADMIN system privilege. To use the purpose object clauses on a JWT or SAML purpose, you must have the USER ADMIN system privilege. To use the certificate clauses you must have the ALTER privilege on the PSE object if you are not the owner of the PSE store. To add or drop a REMOTE SOURCE purpose you must have the system privilege CREATE SOURCE.

## Examples

The following example shows how to alter an existing PSE store to set a custom certificate along with a certificate trust chain (certificate content shortened):

```sql
ALTER PSE example_pse SET OWN CERTIFICATE
-----BEGIN RSA PRIVATE KEY-----
MIIFDjBABgkqhkiG9w0BBQ0wMzAbBgkqhkiG9w0BBQwwDgQIS2qgprFqPxECAggA
.... MANY LINES LIKE THAT ....
H0ga/iLNvWYexG7FHLRiq5hTj0g9mUPEbeTXuPtOkTEb/0ckVE2iZH9l7g5edmUZ=
-----END RSA PRIVATE KEY-----
-----BEGIN CERTIFICATE-----
MIIDXTCCAkWgAwIBAgIJAJC1HiIAZAiIMA0GCSqGSIb3DQEBBQUAMEUxCzAJBgNV
.... MANY LINES LIKE THAT ....
B7xxt8BVc69rLeHV15A0qyx77CLSj3tCx2IUXVqRs5mlSbq094NBxsauYcm0A6Jq==
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
MIID4ppoB7xxAwIBAgIJAJCWgAIAZAiIMA0GCSqGSIb3DQEBBQUAMEUxCzAJ3tCx2
.... MANY LINES LIKE THAT ....
A34ppoB7xxtanU8BVc69rLeHV15A0qyx77CLSj3tCx2IUXVqRs5mlSbuYcm0A6JvA==
-----END CERTIFICATE-----
```

The following example adds the provider provider1 to the mypse1 PSE.

```sql
ALTER PSE pse1 ADD PROVIDER provider1;
```

The following example adds the host host1.sap.corp to the mypse2 PSE.

```sql
ALTER PSE mypse2 ADD HOST 'host1.sap.corp';
```

The following example removes the provider provider1 from the mypse1 PSE.

```sql
ALTER PSE pse1 DROP PROVIDER provider1;
```

The following example removes the host host1.sap.corp from the mypse2 PSE.

```sql
ALTER PSE mypse2 DROP HOST 'host1.sap.corp';
```

The following example adds another remote source to a PSE that has the purpose REMOTE SOURCE.

```sql
ALTER PSE HDB_PSE ADD REMOTE SOURCE HDB_ADM;
```

## Related Information

CREATE JWT PROVIDER Statement (Access Control) [→](CREATE-JWT-PROVIDER-Statement-Access-Control.md) CREATE SAML PROVIDER Statement (Access Control) [→](CREATE-SAML-PROVIDER-Statement-Access-Control.md) CREATE X509 PROVIDER (Access Control) [→](CREATE-X509-PROVIDER-Access-Control.md) SET PSE Statement (System Management) [→](SET-PSE-Statement-System-Management.md) PSE_PURPOSE_OBJECTS System View [→](../../../6-System-Views-Reference/6.01-System-Views/PSE_PURPOSE_OBJECTS-System-View.md) CREATE REMOTE SOURCE Statement (Access Control) [→](CREATE-REMOTE-SOURCE-Statement-Access-Control.md) UNSET PSE Statement (System Management) [→](UNSET-PSE-Statement-System-Management.md)
