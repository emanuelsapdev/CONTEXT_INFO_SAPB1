# 4.10.1.27 ALTER X509 PROVIDER (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 651–653

Alters an X.509 provider in the SAP HANA database.

## Syntax

```sql
ALTER X509 PROVIDER <x509_provider_name>
   { SET { [ <issuer_clause> ] [ <matching_rules_clause> ] }
   | UNSET MATCHING RULES
```

## Syntax Elements

#### x509_provider_name

Specifies the identifier of an X.509 provider to be modified.

```sql
<x509_provider_name> ::= <simple_identifier>
```

#### issuer_clause

Sets the issuer distinguished name for the X.509 provider.

```sql
<issuer_clause> ::= ISSUER <issuer_distinguished_name>
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

Setting new matching rules replaces existing rules for the provider. **UNSET MATCHING RULES** Removes matching rules for the provider. If a user is mapped to the provider using a wildcard (ANY) subject, you cannot unset the matching rules.

## Description

For the SET clause, at least one of the two optional parameters must be specified.

## Permissions

Only database users with the USER ADMIN system privilege are allowed to change X.509 providers.

## Examples

Change the issuer of the MyProvider X.509 provider.

```sql
ALTER X509 PROVIDER MyProvider SET ISSUER 'CN=DigiCert Global Root CA,
OU=www.digicert.com, O=DigiCert Inc, C=US'
```

Remove the matching rules of the MyProvider X.509 provider.

```sql
ALTER X509 PROVIDER MyProvider UNSET MATCHING RULES
```

## Related Information

CREATE X509 PROVIDER (Access Control) [→](CREATE-X509-PROVIDER-Access-Control.md) DROP X509 PROVIDER (Access Control) [→](DROP-X509-PROVIDER-Access-Control.md) X509_PROVIDERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/X509_PROVIDERS-System-View.md) X509_PROVIDER_RULES System View [→](../../../6-System-Views-Reference/6.01-System-Views/X509_PROVIDER_RULES-System-View.md) X509_USER_MAPPINGS System View [→](../../../6-System-Views-Reference/6.01-System-Views/X509_USER_MAPPINGS-System-View.md)
