# 4.10.1.15 ALTER SAML PROVIDER Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 453–455

Changes the properties of the specified SAML provider.

## Syntax

```sql
ALTER SAML PROVIDER <saml_provider_name>
 { <subject_issuer_clause>
   | <user_creation_clause>
   | <entityid_clause>
   | <case_clause>
 }
```

## Syntax Elements

#### saml_provider_name

Specifies the SAML provider to alter.

```sql
<saml_provider_name> ::= <simple_identifier>
```

#### subject_issuer_clause

Sets the SAML identity provider information.

```sql
<subject_issuer_clause> ::=
   SET SUBJECT <subject_distinguished_name> ISSUER <issuer_distinguished_name>
```

#### subject_distinguished_name

Specifies the subject name provided in the certificate of the SAML identity provider.

```sql
<subject_distinguished_name> ::= <string_literal>
```

#### issuer_distinguished_name

Specifies the issuer name provided in the certificate of the SAML identity provider.

```sql
<issuer_distinguished_name> ::= <string_literal>
```

#### user_creation_clause

Enables or disables user creation.

```sql
<user_creation_clause> ::= {ENABLE | DISABLE} USER CREATION
```

When enabled, and a connection is opened for an unknown user using the SAML provider identified by `<saml_provider_name>`, an implicit user creation occurs.

#### entityid_clause

Sets or unsets the entity ID of the SAML identity provider.

```sql
<entityid_clause> ::= [ UNSET ] ENTITY ID <string_literal>
```

#### case_clause

Specifies whether the user mapping is checked case sensitive (default) or insensitive.

```sql
<case_clause> ::= CASE { SENSITIVE | INSENSITIVE } IDENTITY
```

## Description

The SAML provider must already exist in the SAP HANA database.

## Permissions

Only database users with the USER ADMIN system privilege are allowed to change SAML providers.

## Example

This example alters the ac_saml_provider.

```sql
ALTER SAML PROVIDER ac_saml_provider
        SET SUBJECT 'CN = wiki.detroit.BCompany.corp,OU = BCNet,O = BCompany,C =
EN'
        ISSUER 'E = John.Do@acompany.com,CN = BCNetCA,OU = BCNet,O = BCompany,C
= EN';
```

This example enables user creation.

```sql
ALTER SAML PROVIDER ac_saml_provider ENABLE USER CREATION;
```

This example makes the case identity insensitive.

```sql
ALTER SAML PROVIDER ac_saml_provider CASE INSENSITIVE IDENTITY;
```

This example removes the entity ID defined for the ac_saml_provider SAML provider.

```sql
ALTER SAML PROVIDER ac_saml_provider UNSET ENTITY ID;
```

## Related Information

SAML_PROVIDERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/SAML_PROVIDERS-System-View.md) CREATE SAML PROVIDER Statement (Access Control) [→](CREATE-SAML-PROVIDER-Statement-Access-Control.md)
