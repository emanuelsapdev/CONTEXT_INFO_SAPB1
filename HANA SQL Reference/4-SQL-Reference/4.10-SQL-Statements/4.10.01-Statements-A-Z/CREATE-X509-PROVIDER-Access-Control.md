# 4.10.1.79 CREATE X509 PROVIDER (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 884–886

Defines an X.509 provider in the SAP HANA database.

## Syntax

```sql
CREATE X509 PROVIDER <x509_provider_name> <issuer_clause>
[ <matching_rules_clause> ]
```

## Syntax Elements

#### x509_provider_name

Specifies the identifier of an X.509 provider to be created. The X.509 provider name must not already be defined.

```sql
<x509_provider_name> ::= <simple_identifier>
```

#### issuer_clause

Sets the issuer distinguished name for the X.509 provider.

```sql
<issuer_clause> ::= WITH ISSUER <issuer_distinguished_name>
<issuer_distinguished_name> ::= <string_literal>
```

#### matching_rules_clause

Specifies one or more rules for matching external identities to database users. A matching rule is a distinguished name where one attribute has a value of ‘\*’. This attribute contains the user name that needs to be matched during logon. All other attributes must match and be in the same order.

Matching rules are tried in the same order they are defined in the provider, and the first one that matches is used.

```sql
<matching_rules_clause> ::= MATCHING RULES
'<subject_distinguished_name_mapping>'
   [, '<subject_distinguished_name_mapping>' ... ]
<subject_distinguished_name_mapping> ::= <string_literal>
```

## Permissions

Only database users with the USER ADMIN system privilege can create an X.509 provider.

## Examples

Create an X.509 provider.

```sql
CREATE X509 PROVIDER MyProvider WITH ISSUER 'CN=DigiCert Global Root CA,
OU=www.digicert.com, O=DigiCert Inc, C=US';
```

Create an X.509 provider with a matching rule.

```sql
CREATE X509 PROVIDER MyProvider WITH ISSUER 'CN=DigiCert Global Root CA,
OU=www.digicert.com, O=DigiCert Inc, C=US'
   MATCHING RULES 'CN=*, OU=SAP SE, C=DE';
```

## Related Information

ALTER X509 PROVIDER (Access Control) [→](ALTER-X509-PROVIDER-Access-Control.md) DROP X509 PROVIDER (Access Control) [→](DROP-X509-PROVIDER-Access-Control.md) X509_PROVIDERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/X509_PROVIDERS-System-View.md) X509_PROVIDER_RULES System View [→](../../../6-System-Views-Reference/6.01-System-Views/X509_PROVIDER_RULES-System-View.md) X509_USER_MAPPINGS System View [→](../../../6-System-Views-Reference/6.01-System-Views/X509_USER_MAPPINGS-System-View.md)
