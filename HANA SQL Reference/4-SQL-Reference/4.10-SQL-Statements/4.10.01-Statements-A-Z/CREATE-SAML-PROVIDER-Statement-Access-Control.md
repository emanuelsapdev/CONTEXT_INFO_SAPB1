# 4.10.1.61 CREATE SAML PROVIDER Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 759–761

Defines a SAML provider in the SAP HANA database.

## Syntax

```sql
CREATE SAML PROVIDER <saml_provider_name> <subject_issuer_clause>
   [ <entityid_clause> ] [ <user_creation_clause> ] [ <case_clause> ]
```

## Syntax Elements

#### saml_provider_name

Specifies the identifier of a SAML provider to be created.

```sql
<saml_provider_name> ::= <simple_identifier>
```

The SAML provider name must not already be defined.

#### subject_issuer_clause

Sets SAML identity provider information.

```sql
<subject_issuer_clause> ::=
 WITH SUBJECT <subject_distinguished_name> ISSUER <issuer_distinguished_name>
```

##### subject_distinguished_name

Specifies the subject name provided in the certificate of the SAML identity provider.

```sql
<subject_distinguished_name> ::= <string_literal>
```

##### issuer_distinguished_name

Specifies the issuer name provided in the certificate of the SAML identity provider.

```sql
<issuer_distinguished_name> ::= <string_literal>
```

#### entityid_clause

Specifies the entity ID of the SAML identity provider.

```sql
<entityid_clause> ::= ENTITY ID <string_literal>
```

#### user_creation_clause

Implicitly creates a user when specified and a connection is opened for an unknown user using the SAML provider identified by `<saml_provider_name>`.

```sql
<user_creation_clause> ::= ENABLE USER CREATION
```

#### case_clause

Specifies whether the user mapping is checked case sensitive (default) or insensitive.

```sql
<case_clause> ::= CASE { SENSITIVE | INSENSITIVE } IDENTITY
```

## Description

A SAML provider is required to provide a SAML connection facility for users.

The `<subject_distinguished_name>` and the `<issuer_distinguished_name>` correspond to the subject and issuer of the X.509 certificate used by the SAML identity provider to sign assertions. The syntax of these names can be found in ISO/IEC 9594-1.

A detailed description of the concepts of SAML can be found in Oasis SAML 2.0.

## Permissions

Only database users with the USER ADMIN system privilege can create a SAML provider.

## Example

Create a SAML provider with the name ac_saml_provider in the database specifying the subject and issuer to belong to ACompany. The entity ID is entity1. The identity checked by the provider is case sensitive.

```sql
CREATE SAML PROVIDER ac_saml_provider
    WITH SUBJECT 'CN = wiki.detroit.ACompany.corp,OU = ACNet,O = ACompany,C = EN'
    ISSUER 'E = John.Do@acompany.com,CN = ACNetCA,OU = ACNet,O = ACompany,C = EN'
    ENTITY ID 'entity1' CASE SENSITIVE IDENTITY;
```

## Related Information

[SAML_PROVIDERS System View](../../../6-System-Views-Reference/6.01-System-Views/SAML_PROVIDERS-System-View.md)
